---
layout: post
title: "Deal Header"
category: "Sales"
icon: "icon-tag"
type: "data_access"
comments: false
description: Access all local purchase orders and their associated unit information
---
---

### Deal Header
---

This data object is used to display the header information and cumulative totals for all deals, open or invoiced, in the Fusion business system.

This information can be found in the Deal program in Fusion.

Note that exactly one record will be displayed for every deal record in Fusion. 

To view the corresponding detail information, join to Deal Detail. This will display all detail items on the given deal and on its corresponding deal packets. To view cumulative totals for the deal packets on the given deal, join to Deal Packet.

#### URL
```

```

<hr>
Field Details...

| **SQL Field Name**           | **Column Description**                                                                                                                       |
|---|---|
| AddDate                      | This field displays the date on which the given deal was added to the system.                                                                |
| AddUser                      | This field displays the username of the user who added the given deal to the system.                                                         |
| Branch                       | This field displays the branch associated with the given deal.                                                                               |
| Commission                   | This field displays the total amount of commission paid out to the salesperson associated with the given deal.                               |
| CompanyName                  | This field displays the company name for the customer on the given deal.                                                                     |
| CustomerNumber               | This field displays the identifying code for the customer on the given deal.                                                                 |
| IsCustomerPickup             | This field displays whether the customer will pick up the units associated with the given deal, rendering delivery unnecessary.              |
| CustomerPO                   | This field displays the purchase order number associated with the customer on the given deal.                                                |
| DealNumber                   | This field displays the deal number of the given deal.                                                                                       |
| DealStatus                   | This field displays the status of the given deal.                                                                                            |
| DeliveryDate                 | This field displays the date on which the units associated with the given deal will be delivered.                                            |
| Department                   | This field displays the department associated with the given deal.                                                                           |
| ExpirationDate               | This field displays the date on which the quote for the given deal will expire.                                                              |
| IsFinancingApproved          | This field displays whether the customer has been approved for financing for the given deal.                                                 |
| IsFinancingRequired          | This field displays whether financing is required for the given deal.                                                                        |
| LastUpdateDate               | This field displays the date on which the given deal was last updated in the system.                                                         |
| LastUpdateUser               | This field displays the username of the user who last updated the given deal in the system.                                                  |
| PaidDate                     | This field displays the date on which the balance for the given deal will be paid.                                                           |
| PaymentMethod                | This field displays the payment method associated with the given deal.                                                                       |
| QuoteDate                    | This field displays the date on which the quote for the given deal was created.                                                              |
| SaleType                     | This field displays the sale type of the given deal.                                                                                         |
| Salesperson                  | This field displays the username of the salesperson associated with the given deal.                                                          |
| SalespersonName              | This field displays the first and last name of the salesperson associated with the given deal.                                               |
| SignDate                     | This field displays the date on which the documents for the given deal were signed by the customer.                                          |
| TaxBasis                     | This field displays whether the tax on the given deal should be calculated based on the local tax region or the tax region for the customer. |
| TaxBody                      | This field displays the tax body associated with the given deal.                                                                             |
| TaxRegion                    | This field displays the tax region associated with the given deal.                                                                           |
| TaxStatus                    | This field displays the tax status associated with the given deal.                                                                           |
| TotalDealAddOnCost           | This field displays the total cost of all deal add ons remaining on the deal.                                                                |
| TotalDealAddOnPrice          | This field displays the total price of all deal add ons remaining on the deal.                                                               |
| TotalDeposits                | This field displays the total of all deposits remaining on the deal.                                                                         |
| TotalDownPayments            | This field displays the total of all down payments remaining on the deal.                                                                    |
| TotalFET                     | This field displays the total FET associated with all units remaining on the deal.                                                           |
| TotalFinanceReserve          | This field displays the total of the finance reserves from the financing remaining on the deal.                                              |
| TotalFinanced                | This field displays the total amount of financing remaining on the deal.                                                                     |
| TotalNonProfitDealAddOnCost  | This field displays the total cost of all deal add ons remaining on the deal, which are not included in the profit calculation.              |
| TotalNonProfitDealAddOnPrice | This field displays the total price of all deal add ons remaining on the deal, which are not included in the profit calculation.             |
| TotalNonProfitUnitAddOnCost  | This field displays the total cost of all unit add ons remaining on the deal, which are not included in the profit calculation.              |
| TotalNonProfitUnitAddOnPrice | This field displays the total price of all unit add ons remaining on the deal, which are not included in the profit calculation.             |
| TotalPayoffs                 | This field displays the total of all payoffs associated with trade in units remaining on the deal.                                           |
| TotalProfit                  | This field displays the total profit from the units and add ons remaining on the deal.                                                       |
| TotalProfitDealAddOnCost     | This field displays the total cost of all deal add ons remaining on the deal, which are included in the profit calculation.                  |
| TotalProfitDealAddOnPrice    | This field displays the total price of all deal add ons remaining on the deal, which are included in the profit calculation.                 |
| TotalProfitPercent           | This field displays the percentage of the total price of the units and add ons remaining on the deal that is considered profit.              |
| TotalProfitUnitAddOnCost     | This field displays the total cost of all unit add ons remaining on the deal, which are included in the profit calculation.                  |
| TotalProfitUnitAddOnPrice    | This field displays the total price of all unit add ons remaining on the deal, which are included in the profit calculation.                 |
| TotalSalesTax                | This field displays the total sales tax remaining on the deal.                                                                               |
| TotalTradeInActualCashValue  | This field displays the total actual cash value for all trade in units remaining on the deal.                                                |
| TotalTradeInAllowance        | This field displays the total allowance for all trade in units remaining on the deal.                                                        |
| TotalUnitAddOnCost           | This field displays the total cost of all unit add ons remaining on the deal.                                                                |
| TotalUnitAddOnPrice          | This field displays the total price of all unit add ons remaining on the deal.                                                               |
| TotalUnitCost                | This field displays the total cost of all units remaining on the deal.                                                                       |
| TotalUnitFinanceReserve      | This field displays the total of the finance reserves from the financing associated with particular units remaining on the deal.             |
| TotalUnitFinanced            | This field displays the total amount of financing associated with particular units remaining on the deal.                                    |
| TotalUnitPrice               | This field displays the total price of all units remaining on the deal.                                                                      |
| IsWorksheet                  | This field displays whether the given deal is marked as a worksheet in Fusion.                                                               |