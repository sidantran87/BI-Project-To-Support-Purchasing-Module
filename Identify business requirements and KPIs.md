# BI-Project-To-Support-Purchasing-Module

# 1. Brief Introduction
In the contemporary business landscape, leveraging data effectively is pivotal for organizational success. The project aims to implement a Business Intelligence (BI) solution to optimize the purchasing processes at Adventure Works, a multinational bicycle manufacturing company. This document outlines the business requirements, goals, and key performance indicators (KPIs) necessary to achieve purchasing excellence.

# 2. Goals and Business Requirements
## General Goals:

- Enhance overall operational efficiency.
- Promote data-driven decision-making.
- Minimize costs and waste.
- Foster a data-centric organizational culture.
## Specific Business Requirements:

### Inventory Management:

- Develop a dashboard showing inventory quantities, product locations, and status.
- Track the number of available products and their safety stock levels.
- Provide insights into inventory management performance.
### Procurement Performance:

- Create dashboards to display average prices and price trends over time.
- Evaluate vendor performance based on pricing, delivery time, and quality.
- Facilitate effective price negotiations with vendors.
### Functional Requirements:

- Real-time data updates for inventory and procurement.
- Ad hoc query capabilities for dynamic data exploration.
- Collaborative decision-making tools for stakeholders.
### Technical Requirements:

- Seamless integration with ERP systems and supplier databases.
- Robust data warehouse design for unified data view.
- Efficient ETL processes for data quality and updates.
- Secure access controls and data encryption.
# 3. KPI Analysis
## Inventory Management:

### Question 1: What is the status of the specific product in terms of quality, quantity, and location?

KPIs:
- Product Quantity
- VendorPerProduct
- CountOfVendor by PostalCode
### Question 2: What is the status of the product in terms of current quantity, safety stock?

KPIs:
- Product Quantity
- SafetyStockLevel
### Question 3: Do we need to make a purchase for the specific product?

KPIs:
- MakePurchase


Formula:
- Product Quantity: present the quantity of each product.
- Count of ProductID: this KPI counts all of the product ID.
- Value on Hand: the monetary value of all of the stocks in the inventory.
- SafetyStockLevel: Safety stock is a buffer of inventory kept to mitigate the risk of stockouts due to variability in demand or lead time.
- MakePurchase: Gives the status of a product whether it needs to be purchased, needs to be considered for purchase or does not need to be purchased.
Formula: MakePurchase = “Urgent” if “Quantity” < “SafetyStock”
= “MakePurchase”  if  “SafetyStock” <= “Quantity” < “ReOrderPoint”
= “NoNeed” if “Quantity” >= “ReOrderPoint”
- VendorPerProduct: The way to find do the product has more than 1 vendor or not. If they are from and under 1 vendor, it means that we are too dependent on that vendor and need to find an alternative supplier or additional supplier.
Formula: VendorPerProduct = Count(Vendor of a specific product)
- CountOfVendor by PostalCode: present the number of vendors related to each postal code. This KPI can help define the nearest or the most suitable vendor based on the location.
## Procurement Performance
### Question 1: Who are our vendors?

KPIs:
- TotalNumberOfPO (indirectly through vendor-related purchase orders)
- AveragePriceByVendor (provides vendor-specific information)
- POSuccessRate (indirectly through successful purchase orders related to vendors)
### Question 2: Which are our best partners, which are our potential vendors?

KPIs:
- POSuccessRate
- POReturnRate
- POLeadTime
- AveragePOLeadTime
- CreditRating
### Question 3: What products do they supply us? Do we have to find the additional or alternative suppliers?

KPIs:
- TotalNumberOfPO (indicates product-specific purchase orders)
- AveragePriceByVendor (indicates products and their pricing by vendor)
- POReturnRate (quality indicator for products from specific vendors)
- VendorPerProduct (indicates dependency on specific vendors, identifying need for alternatives)
### Question 4: Can we choose the vendors based on some indicators such as price, lead time, quality or order rejected by vendor, product return rate?

KPIs:
- AveragePriceByVendor
- POSuccessRate
- POReturnRate
- POLeadTime
 -AveragePOLeadTime
- CreditRating
### Question 5: What is the appropriate price for the product?

KPIs:
- AveragePrice
- AveragePriceByVendor
### Question 6: What is the trend in price of the product? How can we choose the right vendor in terms of pricing?
KPIs:
- AveragePrice
- AveragePriceByVendor
### Formula:
- AveragePrice
- AveragePriceByVendor
Key performance indicators:
- TotalNumberOfPO: present the number of purchase orders.
- TotalPurchaseAmount: present the total purchase amount that the company spent.
- TotalTaxAmount: present the total tax amount from all purchase orders.
- AverageTaxAmountPerPO: present the average tax amount of each purchase order.
Formula: AverageTaxAmountPerPO = TotalTaxAmountTotalNumberOfPO
- AveragePrice: present the average price of each product.
- AveragePriceByVendor: present the average price of each product by each vendor. These KPIs can be used to find if the given price from the supplier is good or not.
- POSuccessRate: show the successful rate of placing a purchase order.
Formula: POSuccessRate = Number of received Purchase orderTotal quantity Purchase orderx100
- POReturnRate: show the percentage of product was rejected and return to the supplier. Shows the quality of a order supplied by a vendor
Formula: POReturnRate =  Total number  of rejected productTotal number  of receivedx100
- POLeadTime: the amount of time between when a purchase order is placed to replenish products and when the order is received in the warehouse. The smaller the PO lead time is the better the supplier is.
Formula: POLeadTime = Received date - Order date
- AveragePOLeadTime: present the average of PO’s lead time.
Formula: AveragePOLeadTime = POLeadTimeTotalNumberOfPO
- CreditRating: Rating whether a vendor is good or not:
Formula: CreditRating 1 = Superior, 2 = Excellent, 3 = Above average, 4 = Average, 5 = Below average


