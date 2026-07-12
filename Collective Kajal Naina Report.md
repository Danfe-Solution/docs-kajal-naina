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
  
  ![[Pasted image 20260712170109.png]]
 
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
  
  ![[Pasted image 20260712170205.png]]
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
  
  ![[Pasted image 20260712170523.png]]
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
![[Pasted image 20260712170611.png]]
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
![[Pasted image 20260712170712.png]]
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
  ![[Pasted image 20260712170811.png]]
  
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
  ![[Pasted image 20260712171104.png]]
## Sales Billing Single Sale to Invoice Flow  
  
## 7. Sales Return  
  Sales Return covers both a plain customer return and a product exchange. Returned items are added back to inventory after validation, and every return or exchange stays linked to the original sales invoice, so its history is fully traceable.  
## Return vs. Exchange Fee  
  
| Type | Fee | Effect |  
| --- | --- | --- |  
| Return | 19% | Deducted from the refund amount |  
| Exchange | 12% | Deducted from the exchanged item's value; remainder becomes part- payment on the new item |  
  On an exchange, the transaction also carries a note referencing the original invoice, so it is clear at a glance that this is an exchange and not a fresh sale.  
## Sales Return Overview  
![[Pasted image 20260712171201.png]]
## Role Overview  
  
| Action | Org Admin | Internal Finance | Store Manager | Sales Team |  
| --- | --- | --- | --- | --- |  
| View Sales Returns / Exchanges | Yes | Yes | Yes | Own transactions |  
| Create Return / Exchange | Yes | Yes | Yes | Yes |  
| View Fee Amounts | Yes | Yes | Yes | Yes |
