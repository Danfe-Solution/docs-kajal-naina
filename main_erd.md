# Tenant Database ERD for CountIt [Jewellery]

Below is the Entity-Relationship Diagram (ERD) for the tenant database, designed for a multi-tenant SaaS jewelry inventory and POS system.

## Mermaid ERD Diagram

```mermaid
erDiagram

    Branches {
        int branch_id PK
        string name
        string currency_code
        bool is_active
        datetime created_at
        datetime updated_at
    }

    POSTerminals {
        int terminal_id PK
        int branch_id FK
        string terminal_code
        string name
        bool is_active
        datetime created_at
    }

    Users {
        int user_id PK
        string email
        string full_name
        string role
        int branch_id FK "nullable"
        bool is_active
        datetime created_at
    }

    Products {
        int product_id PK
        string sku UK
        string name
        string base_unit
        int tax_category_id FK
        bool is_discountable
        bool allow_price_change
        bool is_active
        datetime created_at
        datetime updated_at
    }

    ProductUnits {
        int unit_id PK
        int product_id FK
        string unit_name
        decimal conversion_factor
        bool is_active
    }

    ProductAttributes {
        int attribute_id PK
        int product_id FK
        string attribute_name
        string attribute_value
    }

    ProductVendorRates {
        int rate_id PK
        int product_id FK
        int vendor_id FK
        string unit
        decimal rate
        date effective_from
        date effective_to
    }

    ProductCustomerTypeRates {
        int rate_id PK
        int product_id FK
        int customer_type_id FK
        decimal rate
        date effective_from
        date effective_to
    }

    ProductOutletRates {
        int rate_id PK
        int product_id FK
        int branch_id FK
        decimal rate
        date effective_from
        date effective_to
    }

    Vendors {
        int vendor_id PK
        string name
        int ledger_id FK
        bool is_active
        datetime created_at
    }

    CustomerTypes {
        int customer_type_id PK
        string name
        string description
    }

    Customers {
        int customer_id PK
        string name
        int customer_type_id FK
        int ledger_id FK
        bool is_active
        datetime created_at
    }

    Suppliers {
        int supplier_id PK
        string name
        int ledger_id FK
        bool is_active
        datetime created_at
    }

    Employees {
        int employee_id PK
        string name
        int ledger_id FK
        bool is_active
        datetime created_at
    }

    Batches {
        int batch_id PK
        int product_id FK
        int branch_id FK
        string batch_no
        decimal quantity
        string created_via
        int created_by_user_id FK
        datetime created_at
        datetime updated_at
    }

    InventoryTransactions {
        int txn_id PK
        int product_id FK
        int batch_id FK
        int branch_id FK
        string txn_type
        decimal quantity
        int reference_id "FK to Sales/Purchases/etc."
        date txn_date
        int created_by_user_id FK
        int approved_by_user_id FK "nullable"
        string approval_status
        text notes
    }

    TaxCategories {
        int tax_category_id PK
        string name
        decimal rate
        bool is_active
    }

    Ledgers {
        int ledger_id PK
        string name
        string type
        string code
        bool is_active
    }

    Sales {
        int sale_id PK
        int branch_id FK
        int terminal_id FK
        int customer_id FK "nullable"
        date sale_date
        decimal total_amount
        decimal tax_amount
        decimal discount_amount
        decimal net_amount
        int created_by_user_id FK
        string status
    }

    SaleItems {
        int sale_item_id PK
        int sale_id FK
        int product_id FK
        int batch_id FK
        decimal quantity
        decimal unit_price
        decimal tax_amount
        decimal discount_amount
        decimal line_total
    }

    Purchases {
        int purchase_id PK
        int branch_id FK
        int vendor_id FK
        date purchase_date
        string invoice_no
        bool is_vat_invoice
        decimal claimable_vat_percent "nullable"
        decimal total_amount
        decimal tax_amount
        decimal net_amount
        string status
    }

    PurchaseItems {
        int purchase_item_id PK
        int purchase_id FK
        int product_id FK
        int batch_id FK "nullable"
        decimal quantity
        decimal unit_price
        decimal tax_amount
        decimal line_total
    }

    CustomerPayments {
        int payment_id PK
        int customer_id FK
        int sale_id FK "nullable"
        date payment_date
        string payment_method
        decimal amount
        decimal tds_amount
        decimal total_amount
        string status
    }

    SupplierPayments {
        int payment_id PK
        int supplier_id FK
        int purchase_id FK "nullable"
        date payment_date
        string payment_method
        decimal amount
        decimal tds_amount
        decimal total_amount
        string status
    }

    PaymentAdditionalHeadings {
        int heading_id PK
        string name
        string type
        string applies_to
        string calculation_type
        decimal value
        string applies_on
        bool is_active
    }

    PaymentHeadingLines {
        int line_id PK
        int payment_id FK
        int heading_id FK
        decimal calculated_amount
    }

    Branches ||--o{ POSTerminals : has
    Branches ||--o{ Users : "users assigned to (optional)"
    Branches ||--o{ ProductOutletRates : "has outlet-specific rates"
    Branches ||--o{ Batches : "holds batches"
    Branches ||--o{ InventoryTransactions : "transactions belong to"
    Branches ||--o{ Sales : "sales belong to"
    Branches ||--o{ Purchases : "purchases belong to"

    POSTerminals ||--o{ Sales : "used for"

    Users ||--o{ Batches : created_by
    Users ||--o{ InventoryTransactions : created_by
    Users ||--o{ InventoryTransactions : approved_by
    Users ||--o{ Sales : created_by

    Products ||--o{ ProductUnits : "has units"
    Products ||--o{ ProductAttributes : "has attributes"
    Products ||--o{ ProductVendorRates : "has vendor rates"
    Products ||--o{ ProductCustomerTypeRates : "has customer-type rates"
    Products ||--o{ ProductOutletRates : "has outlet rates"
    Products ||--o{ Batches : "has batches"
    Products ||--o{ InventoryTransactions : "involved in"
    Products ||--o{ SaleItems : "sold as"
    Products ||--o{ PurchaseItems : "purchased as"

    TaxCategories ||--o{ Products : "categorizes"

    Vendors ||--o{ ProductVendorRates : "has rates for products"
    Vendors ||--o{ Purchases : "supplies"

    CustomerTypes ||--o{ Customers : "categorizes"
    CustomerTypes ||--o{ ProductCustomerTypeRates : "used in rates"

    Customers ||--o{ Sales : "makes purchases"
    Customers ||--o{ CustomerPayments : "makes payments"

    Suppliers ||--o{ Purchases : "supplies"
    Suppliers ||--o{ SupplierPayments : "receives payments"

    Employees ||--o{ Ledgers : "linked to ledger"

    Ledgers ||--o{ Customers : "linked"
    Ledgers ||--o{ Suppliers : "linked"
    Ledgers ||--o{ Employees : "linked"
    Ledgers ||--o{ Vendors : "linked"

    Batches ||--o{ InventoryTransactions : "tracked via"
    Batches ||--o{ SaleItems : "sold from"
    Batches ||--o{ PurchaseItems : "created via"

    Sales ||--o{ SaleItems : "contains"
    Sales ||--o{ CustomerPayments : "paid via"

    Purchases ||--o{ PurchaseItems : "contains"
    Purchases ||--o{ SupplierPayments : "paid via"

    CustomerPayments ||--o{ PaymentHeadingLines : "has additional headings"
    SupplierPayments ||--o{ PaymentHeadingLines : "has additional headings"

    PaymentAdditionalHeadings ||--o{ PaymentHeadingLines : "used in"
