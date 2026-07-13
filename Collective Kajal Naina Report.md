## System Overview  
  
## Introduction  
  
This system is built to help a jewellery business keep track of everything in one place — what materials come in, what gets made from them, what is sitting in stock right now, and what has been sold. The guiding idea behind the whole system is simple: nothing can be sold unless it was first bought as raw material and then made into a finished piece.  
  
## The Core Idea  
  
- Product Management defines what can be sold.  
-  Purchase Management brings raw material into the business.  
- Purchase Return sends unwanted or incorrect material back to a supplier.  
- Production turns raw material into a finished, sellable piece.  
- Inventory keeps an automatic, always-current count of everything.  
- Sales & Billing is where a customer finally takes something home.  
- Sales Return handles what happens if that customer brings it back.  
## Objective of the System  
  
In plain terms, this system exists to:  
- Track every piece of stock precisely — not just how many rings exist, but exactly which batch, which purchase or production run it came from, and what it is actually made of.  
- Connect the whole chain — a sale traces back to the exact batch it came from, which traces back to the production job, which traces back to the raw material purchase that started it.  
- Support more than one outlet — stock, sales, and reporting all work across multiple warehouses.  
- Keep the accounting honest and automatic — purchases, sales, returns, and production update the books and inventory valuation on their own.  
- Control who sees what — cost and purchase-price information stays hidden from sales-floor roles, throughout every module.  
## Role-Based Dashboard & Menu  
  
Every user lands on a Dashboard right after logging in — but the dashboard and the sidebar menu are both generated per role, not shared. Org Admin, Internal Finance, Store Manager, and Sales Team each see a different set of widgets and a different menu, built around what that role actually needs to do.  
  
<img width="1064" height="584" alt="image" src="https://github.com/user-attachments/assets/9d97a2c6-4d41-4fdf-b0e5-ecddc2bfcdfd" />

 
## The Four Roles  
  
| Role | What They See |  
| --- | --- |  
| Org Admin | Full oversight — every widget, every menu item, nothing hidden. |  
| Internal Finance | Cost, accounting, and supplier-facing widgets and reports. |  
| Store Manager | Day-to-day outlet operations, without full financial/cost access. |  
| Sales Team | Customer-facing tools to sell and serve, with cost/purchase price hidden. |  
  
## 1. Product Management  
  
This is where every item the business sells gets set up — its name, price, tax treatment, and the specific details that matter for jewellery, such as pearl type, metal karat, or stone quality. Product Management deals only with finished goods — never with the raw materials themselves.  
  
Setting products up correctly always follows the same three-step order, because each step depends on the one before it:  
  
## Attribute Menu  
  - A master list of every Pearl, Metal, and Stone detail the business uses is added first. This is the mandatory starting point — nothing else can be set up before this exists.  
  
## Category   
  - Categories such as Ring or Necklace are created next, and each one is told which of those attribute types actually apply to it, along with default tax and discount rules.  
  
## Product Creation  
  - Individual products are added last. Because the first two steps already exist, a new product automatically shows only the fields relevant to its category, with tax and discount settings already filled in.  
  
## What Gets Captured for Every Product  
  - Basic details — name, unique code, type, category/sub-category, and unit of measure.  
  - Pricing — estimated selling price and purchase price, which can differ across units.  
  - A unique identifying code and barcode for quick lookup at the point of sale.  
  - Whether the item is taxable, and at what rate; whether a discount can be applied.  
  - The specific Pearl, Metal, or Stone attributes relevant to its category.  
## Combo Products  
  
A product can be marked as a Combo with a simple Yes/No toggle, used when the item being sold is really a bundle of a few other products offered together.  
  
## Role Overview  
  
| Action | Org Admin | Internal Finance | Store Manager | Sales Team |  
| --- | --- | --- | --- | --- |  
| View product list | Yes | Yes | Yes | Yes |  
| Create / Edit product | Yes | Yes | Yes | No |  
| Manage Categories / Sub-Categories | Yes | Yes | Yes | No |  
| Manage Attributes | Yes | Yes | Yes | No |  
| Print Barcode | Yes | Yes | Yes | No |  
## Product Management Overview  
  
<img width="975" height="566" alt="image" src="https://github.com/user-attachments/assets/2ed10385-437d-41de-9f84-cb72a5e8b4f4" />

## 2. Purchase Management  
  
Purchase Management is how raw material — Pearl, Metal, or Stone — is bought from a supplier. It can also record a Buy-Back, which is when a finished item already sold to a customer is repurchased back from them at a reduced value.  
## How a Purchase Is Recorded  
### Select the Supplier  
- Choose which supplier or individual the purchase is from, and whether it is a virtual or physical transaction.  
### Add the Items  
  - Each item being bought — products, material, or a Buy-Back finished good — is added with its own rate and quantity.  
### Add Extra Charges  
  - Costs like Freight, Insurance, Transport, Wages, or Import Charges are added as their own lines, flat or as a percentage.  
### Mark VAT  
  - Two Yes/No choices are made for the bill: whether VAT applies, and whether it can be claimed back.  
### Save the Purchase  
  - The system spreads every extra charge fairly across all items on the bill, and generates one batch number for the whole purchase.  
## Key Rules to Remember  
  
- Every purchase bill gets its own single batch number, shared by every item on it.  
- Buying the same material again later — even the very same product — always starts a brand-new, separate batch. It is never merged with earlier stock.  
-  Extra charges are not locked in once the purchase is saved — they can still be added or adjusted afterwards, and the cost is automatically redistributed across the batch.  
-  Discount and VAT are each a simple Yes/No setting on the purchase.  
  
Once saved, a supplier payment can be recorded, or a purchase return created if material needs to be sent back.  
## Role Overview  

| Action | Org Admin | Internal Finance | Store Manager | Sales Team |  
| --- | --- | --- | --- | --- |  
| View Purchases | Yes | Yes | Yes | No |  
| Create / Edit Purchases | Yes | Yes | No | No |  
| View Landed Cost | Yes | Yes | No | No |  
| Mark VAT Applied / Claimable | Yes | Yes | No | No |  
| Create Purchase Return | Yes | Yes | No | No |  
| Record Supplier Payment | Yes | Yes | No | No |  
## Purchase Management Overview  
  
<img width="975" height="517" alt="image" src="https://github.com/user-attachments/assets/b70c5c95-b321-4612-8610-17034601b26e" />

## 3. Purchase Return  
  
A Purchase Return is created whenever stock is sent back to a supplier — with or without the original purchase bill. With a bill, the supplier and the return amount are auto-suggested from that purchase; without one, both are entered manually.  
  
Either way, the returned quantity is deducted from the same batch the stock originally came in on, and the record stays permanently linked to that supplier for their transaction history.  
  
*With Bill vs. Without Bill*  

| Feature  | With Bill                           | Without Bill      |     |
| -------- | ----------------------------------- | ----------------- | --- |
| Supplier | Auto-filled from the bill           | Selected manually |     |
| Batch    | Selected from the bill's line items | Entered manually  |     |
| Amount   | Auto-suggested from the purchase    | Entered manually  |     |
## Purchase Return Overview  
<img width="856" height="506" alt="image" src="https://github.com/user-attachments/assets/1bccbde5-a809-4227-9b2a-9381298fdebe" />

## Role Overview  
  
| Action | Org Admin | Internal Finance | Store Manager | Sales Team |  
| --- | --- | --- | --- | --- |  
| View Purchase Returns | Yes | Yes | No | No |  
| Create Purchase Return | Yes | Yes | No | No |  
| View Suggested / Landed Amount | Yes | Yes | No | No |  
  
## 4. Production  
  
Production is the process that turns raw material into an actual finished piece of jewellery. Nothing purchased — pearl, gold, silver, or stone — can be sold on its own; it only becomes a sellable item once a Production Job is run.  
  
Running a job decreases the exact raw-material batches consumed and creates a new batch for whatever is produced. The same screen also handles Karat Conversion — turning higher-karat gold, or purer silver, into a lower-karat/purity batch by adding alloy — since that conversion is treated as its own production job rather than a step buried inside another one.  
  
## Two Kinds of Production Formula  
  
| Formula Type | What It Consumes | What It Produces |  
| --- | --- | --- |  
| Finished-Goods Formula | Pearl / Metal / Stone raw materials, at a specific karat or attribute | A sellable finished-goods batch (Necklace, Ring, etc.) |  
| Karat Conversion Formula | Higher-karat gold (or higher-purity silver) + alloy | A new batch of the lower-karat gold or lower-purity silver |  
  
Both run through the same steps: if a formula needs a karat/purity batch that doesn't exist yet, the user runs the matching Karat Conversion Formula first, then returns to run the original formula. Every run also records a manually entered Loss ("Jarti") figure and a Making Charge, and automatically posts an accounting voucher once executed.  
## Production Overview  
<img width="959" height="567" alt="image" src="https://github.com/user-attachments/assets/8c8d1805-18e3-4078-b9cb-5703b1da05b6" />

## Role Overview  
| Action                                    | Org Admin | Internal Finance | Store Manager | Sales Team |
| ----------------------------------------- | --------- | ---------------- | ------------- | ---------- |
| View Production Formulas                  | Yes       | Yes              | Yes           | Yes        |
| Create / Edit Production Formulas         | Yes       | Yes              | Yes           | No         |
| Run Production                            | Yes       | Yes              | Yes           | No         |
| Configure Gold / Silver Conversion Ratios | Yes       | Yes              | No            | No         |
  
## 5. Inventory  
  
Inventory is simply the live, always-current record of everything the business has in stock. It has no "add stock" button of its own — every number it shows comes automatically from what happens in the other parts of the system.  
## Where Every Number Comes From  
  - Opening Stock and Purchase — add raw material into stock.  
  - Production — takes raw material out and puts a newly finished item in.  
  - Sales — takes a finished item out, but only once it has actually been delivered.  
  - Returns and Stock Adjust — adjust the count whenever something comes back or a mistake needs fixing.  
## Tracked by Batch  
  - Every batch — from Opening Stock, a Purchase, or a Production run — is tracked individually, so stock from different purchases is never mixed together even if it is the same product.  
  - For each batch, the system keeps a running record of opening quantity, quantity purchased, produced, sold, returned, any manual correction, and the current balance.  
## Organised by Warehouse  
  
Every batch belongs to exactly one warehouse or outlet at a time. Stock can be searched and filtered by warehouse, batch number, product, or attribute, and a Stock Transfer is the only event that moves stock from one warehouse to another.  
## Good to Know  
  - Selecting a batch during a sale reserves it, but does not remove it from Inventory yet.  
  - Cost and purchase-value figures are kept hidden from the Store Manager and Sales Team roles, everywhere in Inventory.  
## Role Overview  
  
| Action | Org Admin | Internal Finance | Store Manager | Sales Team |  
| --- | --- | --- | --- | --- |  
| View Inventory Ledger (qty, attributes) | Yes | Yes | Yes | Yes |  
| View Purchase / Cost Value per Batch | Yes | Yes | No | No |  
| View Batch Transaction History | Yes | Yes | Yes | No |  
| Filter by Warehouse | Yes | Yes | Yes | Yes |  
## Inventory Management Overview  
<img width="975" height="520" alt="image" src="https://github.com/user-attachments/assets/a50cf29f-29e7-470f-b11c-d525ca6cd971" />

## 6. Sales & Billing  
  
This is where a sale actually happens — from choosing a customer to generating the final invoice. It brings together product lookup, batch-level stock selection, automatic discount and tax calculation, advance payments, and delivery tracking.  
## How a Sale Is Created  
## Select the Customer 
- Start a new invoice by choosing who the sale is for. 
## Search and Select the Product  
  -  Look the item up by name or code, with a read-only view of its Pearl, Metal, and Stone composition. Multiple products can be added to one sale.  
### Choose the Batch
- Pick the specific batch the item is coming from. If nothing is available, a Backorder is created instead.  
## Apply Discount & Tax  
  - A discount can be applied before tax, and tax is calculated automatically based on the item's composition.  
## Record Advance Payment & Notes  
  - An advance payment can optionally be recorded, and a note added for the customer if needed.  
## Save the Invoice  
  - A unique invoice number is generated. Payment Status and Delivery Status both begin tracking from this point.  
## Discount & Tax — Only Where They Apply  
  - Discount and VAT apply only to the applicable items like Pearl, Stone, and Labour/Wages value — never to Gold or Silver — and are always applied before tax.  
## Payment and Delivery — Tracked Independently  
  - Payment Status — Unpaid, Partially Paid, or Paid.  
  - Delivery Status — Not Delivered, or Delivered.  
## The Rule That Ties Sales to Inventory  
- Saving the invoice reserves the stock for that batch — it does not remove it from Inventory yet. 
- The item's quantity is only actually deducted once it is marked Delivered.  
- A sale can be fully paid for and still sitting in Inventory until it physically leaves the shop.  
- If an item is out of stock at the time of sale, it becomes a Backorder, completed once stock arrives through a Purchase.  
## Role Overview  
  
| Action | Org Admin | Internal Finance | Store Manager | Sales Team |  
| --- | --- | --- | --- | --- |  
| Create Sale / Bill | Yes | Yes | Yes | Yes |  
| View Purchase / Cost Price | Yes | Yes | No | No |  
| Select Inventory Batch | Yes | Yes | Yes | Yes |  
| Apply Discount | Yes | Yes | Yes | Yes |  
| Create Backorder | Yes | Yes | Yes | Yes |  
| Mark as Delivered | Yes | Yes | Yes | No |  
| View Client Dues Report | Yes | Yes | Yes | Yes |  
## Sales & Billing Overview  
<img width="870" height="623" alt="image" src="https://github.com/user-attachments/assets/e37f5baf-d2d9-4313-b70e-f355b96310b9" />

## 7. Sales Return  
  Sales Return covers both a plain customer return and a product exchange. Returned items are added back to inventory after validation, and every return or exchange stays linked to the original sales invoice, so its history is fully traceable.  
## Return vs. Exchange Fee  
  
| Type | Fee | Effect |  
| --- | --- | --- |  
| Return | 19% | Deducted from the refund amount |  
| Exchange | 12% | Deducted from the exchanged item's value; remainder becomes part- payment on the new item |  
  On an exchange, the transaction also carries a note referencing the original invoice, so it is clear at a glance that this is an exchange and not a fresh sale.  
## Sales Return Overview  
<img width="959" height="567" alt="image" src="https://github.com/user-attachments/assets/329731c8-36c3-4e1a-9f46-a3c13d84077d" />

## Role Overview  
  
| Action | Org Admin | Internal Finance | Store Manager | Sales Team |  
| --- | --- | --- | --- | --- |  
| View Sales Returns / Exchanges | Yes | Yes | Yes | Own transactions |  
| Create Return / Exchange | Yes | Yes | Yes | Yes |  
| View Fee Amounts | Yes | Yes | Yes | Yes |


## **8. Stock Adjustment**  
  
Stock Adjustment is for occasional tasks to check, verify, and correct mismatches between physical stock and system stock. A note, with a file attachment, covering the product SKUs and their related inventory batch numbers, is used to track and manage this.  
  
## **What This Module Covers**  
  
- Stock Adjustment is for **occasional tasks** to check, verify, and correct mismatches between **physical stock and system stock.**  
- **Approved** returned or exchanged products should be added back to inventory with the appropriate batch number and stock quantity.  
## **How an Adjustment Is Recorded**  
### **Create Adjustment**  
- Opens a form that can hold multiple product  / batch lines at once.  
### **Enter Physical vs. System Count**  
- For each line, enter the physical quantity counted and compare it with the system quantity.  
### **Attach a Supporting File**  
- Supporting files, such as photos or signed count sheets, can be attached for each discrepancy.  
### **Add a Reason**  
- A short explanation of the discrepancy is added alongside the file.  
### **Submit**  
- The Inventory  Balance Qty is adjusted per line to match the corrected figure.  
### **Increase vs. Decrease**  
| Variance     | Meaning                                    | Example                                                |
| ------------ | ------------------------------------------ | ------------------------------------------------------ |
| Positive (+) | Physical count is higher than system count | Extra stock found, previously unrecorded               |
| Negative (−) | Physical count is lower than system count  | Shrinkage, damage, theft, miscount at an earlier stage |
  
Both directions post as an adjustment against the batch's Balance Qty — the memo and reason field is what distinguishes them, and both are treated the same way structurally.  
  
## **Stock Adjustment Overview**  
<img width="975" height="445" alt="image" src="https://github.com/user-attachments/assets/b625311a-da86-4315-ada6-3fbae6a5c58d" />

## **Role Overview**  
  
|**Action**|**Org Admin**|**Internal Finance**|**Store Manager**|**Sales Team**|  
|---|---|---|---|---|  
|View Stock Adjustments|**Yes**|**Yes**|**Yes**|**No**|  
|Create Adjustment|**Yes**|**Yes**|**Yes**|**No**|  
|Attach Files|**Yes**|**Yes**|**Yes**|**No**|


## **9. Opening Stock Management**  
  Opening Stock is used to record the existing jewellery and raw material stock before the system starts being used . It t is a one-time setup performed by the **Org Admin** during the initial system setup.  
## **What This Module Covers**  
-  Opening Stock captures **existing stock inventory items** before proper Sales or Purchase entry begins.  
## **How an Opening Stock Entry Is Recorded**  
### **Choose Item/product or material**  
- The **Org Admin** selects the materials or a finished product.  
### **Assign Attributes**  
- Each stock line uses the same attribute structure (Pearl, Metal, or Stone details) used throughout the system.  
### **Enter Opening Quantity & Valuation**  
- For each line, the current quantity and its valuation rate are entered to establish the initial inventory value.  
### **Add As Many Lines of materials As Needed**  
 - A single Opening Stock entry can contain multiple lines for all available raw materials and finished products.  
### **Save**  
- A batch number is generated, and the quantity now shows up in Inventory as this batch's Open Qty.  
### **Raw Material vs. Finished Goods — An Important Difference From Purchase**  
  
- Normally, finished jewellery is created through the **Production** process by converting raw materials or from purchase of products.  
-  **Opening Stock** is the only exception to this rule during the initial system setup.  
-  It allows existing finished jewellery and materials to be added directly into the system.  
- This ensures all stock already available at go-live is recorded without creating Production entries.  
  
## **Opening Stock Overview**  
<img width="975" height="431" alt="image" src="https://github.com/user-attachments/assets/78ee43c1-edaa-4393-8c9f-71c29de4c473" />

## **Role Overview**  
  
|**Action**|**Org Admin**|**Internal Finance**|**Store Manager**|**Sales Team**|  
|---|---|---|---|---|  
|Create Opening Stock<br>Entry|**Yes**|**No**|**No**|**No**|  
|View Opening Stock List|**Yes**|**Yes**|**Yes**|**Yes**|  
|Edit / Delete Existing Entry|**Yes**|**No**|**No**|**No**|

## **10. Stock Transfer**  
  
Stock Transfer is how stock physically moves between outlets. It sits on top of everything else already established — batch tracking, Pearl/Metal/Stone attributes, and multi-outlet support — and is the only event that moves stock, and its full batch history, from one warehouse to another.  
## **What This Module Covers**  
-  **Stock transfer between outlets** can be made.  
## **How a Transfer Is Recorded**  
### **Start a Transfer**  
- Open Item Transfer Create from the Item Transfer List, which shows every transfer already made — From Outlet, To Outlet, Date, Status.  
### **Select From Outlet and To Outlet**  
- Choose the source warehouse the stock is currently in, and the destination it is being sent to.  
### **Add Products & Select Batch**  
- Search by SKU or name, then select the specific batch being moved — not just "10 units of this product," but the exact batch, since a batch carries its own attribute values and cost history that must travel with it.  
### **Enter Quantity**  
- Enter the quantity to move from that batch, and repeat for as many products or batches as the transfer includes.  
### **Save**  
- The transfer is recorded, and the item(s) are logged as moving from one outlet's inventory to the other's.  
### **Item Transfer Detail**  
- Every transfer has its own detail screen, showing the full record: items, batches, quantities, from/to outlets, and current status.  
## **Stock Transfer Overview**  
<img width="975" height="391" alt="image" src="https://github.com/user-attachments/assets/bd622970-f85f-4900-9930-6d76cc3f569c" />

## **Role Overview**  
  
|**Action**|**Org Admin**|**Internal Finance**|**Store Manager**|**Sales Team**|  
|---|---|---|---|---|  
|View Transfers|**Yes**|**Yes**|**Yes**|**No**|  
|Create / Edit Transfer|**Yes**|**Yes**|**Yes**|**No**|  
|Confirm Receipt (if two-<br>step is adopted)|**Yes**|**Yes**|**Yes (own outlet**<br>**only)**|**No**|

## **10. Supplier Management** 
Supplier Management is where every vendor the business buys raw material from — or sells a Buy-Back to — is set up and kept on record. Once a supplier exists, every Purchase and Purchase Return raised against them stays permanently linked to that record.
## **What This Module Covers**
- Supplier master data: **Name, Contact Person, Phone Number, Email, Address, PAN/VAT Number.**
- Suppliers can be **added, edited, activated, or deactivated.**
- Every **Purchase transaction** is linked to the respective supplier.
- Every **Purchase Return** is linked to the respective supplier.

## **How a Supplier Is Set Up**
### **Add Supplier**
- Enter the core details — Name, Contact Person, Phone Number, Email, Address, and PAN/VAT Number (used for tax and import documentation)


### **Save**
- The Supplier Detail screen is created. From here on, it automatically accumulates every Purchase and Purchase Return linked to this supplier, shown as two lists on the same screen.

### Transaction Detail of Supplier
- Clicking any Purchase row opens the full Purchase Detail screen for that bill; clicking any Purchase Return row opens the full Purchase Return Detail screen — each governed by its own role visibility rules.

| **4** | **Activate / Deactivate**<br><br>A status toggle is available from the list or detail screen. Deactivating a supplier hides them from the dropdown on new Purchase entries, while all their historical purchases and returns remain fully visible and untouched. |
## **Supplier Management Overview**

<img width="975" height="431" alt="image" src="https://github.com/user-attachments/assets/9d0bff17-53d2-432b-ae1c-e7d351fccd4e" />


## **Role Overview**

| **Action** | **Org Admin** | **Internal Finance** | **Store Manager** | **Sales Team** |
| --- | --- | --- | --- | --- |
| View Supplier List / Detail | **Yes** | **Yes** | **No** | **No** |
| Create / Edit Supplier | **Yes** | **Yes** | **No** | **No** |
| Activate / Deactivate Supplier | **Yes** | **Yes** | **No** | **No** |
| View Linked Purchase / Return History | **Yes** | **Yes** | **No** | **No** |


# **11. Tax Management**

Tax Management is where VAT and Craftsmanship Tax get set up, and where the day's fluctuating gold and silver rate gets entered. Once configured, Sales Billing pulls these numbers automatically — nobody calculates tax by hand at the counter.

## **What This Module Covers**

- The system keeps track of which products are **taxable and non-taxable.**
- **Pearls and Stones carry 13% VAT.**
- **Craftsmanship (Labour) Tax is 1.5% on Gold.**
- VAT percentage is **configurable per product.**
- The system supports **worker/service tax, where applicable.**
- Tax, including Craftsmanship Tax, is **calculated automatically at billing**, based on a **manually entered daily rate.**
- All tax rates stay **configurable** for future changes.

## **How Tax Gets Set Up and Applied**

### **Configure the Base Rules**
- Org Admin or Internal Finance sets VAT % on Pearl and Stone, Craftsmanship % on Gold, and any worker/service tax rules.


### **Rates Save Immediately**
- Once saved, these are the numbers Sales Billing will use automatically — nobody enters or calculates tax manually at the point of sale.


### **Tax Calculates at Billing**
- VAT (on Pearl/Stone) and Craftsmanship Tax (on Gold) calculate automatically against whichever rate and percentage are currently active.


## **How This Connects to Product Management**

Product Management already lets an individual product carry its own tax rate, overriding its category's default. Tax Management is where those defaults — 13% VAT, 1.5% Craftsmanship — are centrally set; Product Management is just where a specific product can be flagged as an exception if it genuinely needs a different rate.

## **Tax Flow Overview**
<img width="1005" height="400" alt="image" src="https://github.com/user-attachments/assets/76f99f65-6325-419b-84df-7e59c1af76b1" />


## **Role Overview**

| **Action** | **Org Admin** | **Internal Finance** | **Store Manager** | **Sales Team** |
| --- | --- | --- | --- | --- |
| View Tax Configuration | **Yes** | **Yes** | **No** | **No** |
| --- | --- | --- | --- | --- |
| Edit Tax % / Rules | **Yes** | **Yes** | **No** | **No** |
| --- | --- | --- | --- | --- |
| Enter Daily Rate | **Yes** | **Yes** | **No** | **No** |
| --- | --- | --- | --- | --- |
| See Tax on an Invoice (result only) | **Yes** | **Yes** | **Yes** | **Yes** |
| --- | --- | --- | --- | --- |


## **12. Customer Management**  
  
Customer Management is where every customer record is captured and used — personal details, billing and shipping information, loyalty points, and a Customer Level tier. Every sale a customer makes links back to their record, which is what builds their purchase history, feeds loyalty points, and powers the Customer Report.  
  
## **What This Module Covers**  
  
- Customer details: **Name, Contact Person, Phone Number, Email, Address, Date of Birth, Anniversary Date, Billing Address, Shipping Address, multiple mobile numbers, Citizenship Number.**  
- Sales transactions link to the customer, and **purchase history is kept.**  
- Billing details: Street Address, City, State, Postal/Pin Code, Country, Email, primary and secondary mobile numbers — or a **Company Name / Position** for a business customer.  
- **Billing and Shipping addresses can be different.**  
- Customers earn **loyalty points** , based on rules the business can configure.  
- Customers carry a **Customer Level** (e.g. Platinum, Gold, Silver).  
- The system keeps customer **social media handles** — Instagram, Facebook, TikTok — where relevant.  
## **How a Customer Is Set Up**  
  
## **Personal Details
- Name, Date of Birth, Anniversary Date, and Citizenship Number are entered first. **Billing Address & Contact 2** Street Address, City, State, Pin Code, Country, primary and secondary mobile numbers, and email.  
## **Shipping Address**  
* A toggle to copy the billing address, or type in a different one — shipping doesn't have to match billing.  
## **Business Customer Fields (Optional)**  
  - Company Name and Position/Designation, for a customer buying on behalf of a business rather than as an individual.  
  
**Assign a Customer Level & Save 5** A tier is assigned and the record is saved. From here, the Customer Detail page fills in on its own — purchase history, loyalty points, notes, and social handles, as they happen over time.  
##  Question — How Loyalty Points Are Calculated**  
  
Everyone agrees loyalty points should exist and follow configurable business rules — but exactly how points are earned still needs to be decided. Three common approaches:  
### **Flat Spend-to-Point Ratio**  
- A fixed rate for every purchase — e.g. 1 point for every set amount spent. Simple and transparent, but doesn't protect margins on low-margin items like raw gold and silver.  
### **Category / Margin-Based**  
- The rate depends on what's bought — high-margin items like finished pieces, diamonds, or pearls earn points; raw metal weight or labour, where margins are tight, earns none. Protects the business, but is more work to build.  
### **Tier-Based Multiplier**  
- The rate depends on the customer's tier — a Platinum customer might earn two or three times what a Regular customer earns for the same spend. Encourages bigger, consolidated purchases, but ties loyalty logic directly to sales logic.  
## **Customer Management Overview**  
<img width="1005" height="442" alt="image" src="https://github.com/user-attachments/assets/011da477-041c-4ed9-abf0-488300f95e78" />



