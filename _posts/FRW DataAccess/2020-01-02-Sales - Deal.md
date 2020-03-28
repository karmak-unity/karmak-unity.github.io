---
layout: post
title: "Deal Detail"
category: "Sales"
icon: "icon-tag"
type: "data_access"
comments: false
description: Access all detail items on all unit sales deals.
---
---

### Deal Detail
---

This data object is used to display all detail items on all unit sales deals.

This information can be found by clicking the detail hyperlinks in the Deal application in the Fusion business system.

 
#### URL
```

```

<hr>
Field Details...

| **SQL Field Name**        | **Column Description**                                                                                                                                                                                                                                                                 |
|---|---|
| AddDate                   | This field displays the date on which the given detail item was added to the deal.                                                                                                                                                                                                     |
| AddUser                   | This field displays the username of the user who added the given detail item to the deal.                                                                                                                                                                                              |
| AmountSubjectToFET        | This field displays, for the given unit detail item, the amount subject to FET ((FET Amount + Tire Tax Credit)/0.12) for the unit on the given deal.                                                                                                                                   |
| Branch                    | This field displays the branch in which the given deal was created.                                                                                                                                                                                                                    |
| BuyRate                   | This field displays, for the given financing detail item, the buy rate associated with the deal financing.                                                                                                                                                                             |
| Cost                      | This field displays the cost of the given detail item on the deal (Cost for Sale Unit, Unit Addon, or Deal Addon, 0 for Trade Unit, FET, Payoff, Deposit, or Financing).                                                                                                               |
| DealHeaderNumber          | This field displays the deal number of the deal that the given detail item was added to.                                                                                                                                                                                               |
| DealPacketNumber          | This field displays the deal packet number of the deal packet that the given detail item was added to.                                                                                                                                                                                 |
| Department                | This field displays the department in which the given deal was created.                                                                                                                                                                                                                |
| Division                  | This field displays the division in which the given deal was created.                                                                                                                                                                                                                  |
| ExemptDelivery            | This field displays, for the given unit detail item, the amount of exempt delivery expenses associated with the given unit.                                                                                                                                                            |
| ExemptEquipment           | This field displays, for the given unit detail item, the amount of exempt equipment expenses associated with the given unit.                                                                                                                                                           |
| FETAmount                 | This field displays, for the given unit detail item, the amount of Federal Excise Tax charged on the sale of the given unit.                                                                                                                                                           |
| FinanceReserve            | This field displays, for the given financing detail item, the finance reserve amount associated with the deal financing.                                                                                                                                                               |
| InventoryType             | This field displays, for the given unit on the deal, the inventory type of that unit.                                                                                                                                                                                                  |
| InvoiceDate               | This field displays, for invoiced deals, the date on which the given deal was invoiced.                                                                                                                                                                                                |
| InvoiceNumber             | This field displays, for invoiced deals, the invoice number for the given deal.                                                                                                                                                                                                        |
| Item                      | This field displays the identifying name of the given detail item (Stock Number for units, FET for FET, Payoff Name for payoffs, Payment Type for deposits, Finance Lender for financing, and the name of the given addon for unit and deal addons).                                   |
| ItemDescription           | This field displays a brief description of the given detail item (Make, Model, and Year for units, FET for FET, Loan Number for payoffs, Payment Description for deposits, Finance Lender Description for financing, and the description of the given addon for unit and deal addons). |
| ItemType                  | This field displays a description identifying which kind of deal detail item is displayed on the given record.                                                                                                                                                                         |
| LastUpdateDate            | This field displays the date on which the given detail item was last updated on the deal.                                                                                                                                                                                              |
| LastUpdateUser            | This field displays the username of the user who last updated the given detail item on the deal.                                                                                                                                                                                       |
| OrderStatus               | This field displays the status of the given deal, and signifies whether it has been invoiced and/or posted to accounting.                                                                                                                                                              |
| Period                    | This field displays, for the given financing detail item, the financing period associated with the deal financing.                                                                                                                                                                     |
| PrePosted                 | This field displays, for the given deposit on the deal, whether it has been preposted to accounting.                                                                                                                                                                                   |
| Price                     | This field displays the price of the given detail item on the deal (Price for Sale Unit, Price \* -1 for Trade Unit, Addon Price for Unit or Deal Addon, FET Amount for FET, Payoff Amount for Payoff, Deposit Amount \* -1 for Deposit, Financing Amount \* -1 for Financing).        |
| Profit                    | This field displays the profit for the given detail item on the deal.                                                                                                                                                                                                                  |
| ProfitCalculation         | This field displays the calculation used to determine the profit for the given item type.                                                                                                                                                                                              |
| ProfitMargin              | This field displays the percentage of the price of the given item that is considered profit.                                                                                                                                                                                           |
| Rate                      | This field displays, for the given financing detail item, the financing rate associated with the deal financing.                                                                                                                                                                       |
| Refunded                  | This field displays, for the given deposit on the deal, whether it has been refunded.                                                                                                                                                                                                  |
| SaleType                  | This field displays, the sale type associated with the given deal.                                                                                                                                                                                                                     |
| StockNumber               | This field displays the stock number of the unit that the given detail item is associated with (not populated for general deal level detail items).                                                                                                                                    |
| TireTaxCredit             | This field displays, for the given unit detail item, the amount of tire tax credit associated with the given unit.                                                                                                                                                                     |
| TradeInActualCashValue    | This field displays, for the given trade unit on the deal, the amount that the trade unit is actually worth.                                                                                                                                                                           |
| TradeInAllowance          | This field displays, for the given trade unit on the deal, the total allowance given to the customer for the trade unit.                                                                                                                                                               |
| TradeInOverUnderAllowance | This field displays, for the given trade unit on the deal, the over/under allowance (Trade In Allowance - Trade In Actual Cash Value) for the trade unit.                                                                                                                              |