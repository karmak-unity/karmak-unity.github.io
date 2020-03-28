---
layout: post
title: "Deal Packet"
category: "Sales"
icon: "icon-tag"
type: "data_access"
comments: false
description: Access all local purchase orders and their associated unit information
---
---


This data object is used to display all deal packet summary information. There is exactly one record returned for every deal packet in Fusion, open or invoiced. To see detail information line by line, join to Sales Deal Detail.

This information can be found in the Deal Packet program within the Fusion business system.

 
#### URL
```
/frw/SalesDealPacket
```

<hr>
Field Details...

| **SQL Field Name**           | **Column Description**                                                                                                                                                                             |
|---|---|
| AddDate                      | This field displays the date on which the given deal packet was added to the system (for invoiced deal packets, displays the date on which the original open deal packet was added to the system). |
| AddUser                      | This field displays the username of the user who added the given deal packet to the system (for invoiced deal packets, displays the username of the user who added the original open deal packet). |
| BillToAddress1               | This field displays the first line of the bill to address for the given deal packet.                                                                                                               |
| BillToAddress2               | This field displays the second line of the bill to address for the given deal packet.                                                                                                              |
| BillToCity                   | This field displays the city of the bill to address for the given deal packet.                                                                                                                     |
| BillToCountry                | This field displays the country of the bill to address for the given deal packet.                                                                                                                  |
| BillToCounty                 | This field displays the county of the bill to address for the given deal packet.                                                                                                                   |
| BillToPostalCode             | This field displays the postal code of the bill to address for the given deal packet.                                                                                                              |
| BillToRegion                 | This field displays the region of the bill to address for the given deal packet.                                                                                                                   |
| BillToTaxBody                | This field displays the tax body that the bill to address for the given deal packet is located within.                                                                                             |
| Branch                       | This field displays the branch associated with the given deal packet.                                                                                                                              |
| Commission                   | This field displays the total commission amount that the salesperson associated with the sale earned from the given deal packet.                                                                   |
| CommissionPostDate           | This field displays the date on which the commission for the given deal packet was posted to accounting.                                                                                           |
| CommissionPostJournal        | This field displays the journal which the commission for the given deal packet is posted against.                                                                                                  |
| CommissionPostMonth          | This field displays the month and year in which the commission for the given deal packet was posted to accounting.                                                                                 |
| CompanyName                  | This field displays the company name of the customer associated with the given deal packet.                                                                                                        |
| ContactAddress1              | This field displays the first line of the address for the contact associated with the given deal packet.                                                                                           |
| ContactAddress2              | This field displays the second line of the address for the contact associated with the given deal packet.                                                                                          |
| ContactCity                  | This field displays the city of the address for the contact associated with the given deal packet.                                                                                                 |
| ContactCountry               | This field displays the country of the address for the contact associated with the given deal packet.                                                                                              |
| ContactCounty                | This field displays the county of the address for the contact associated with the given deal packet.                                                                                               |
| ContactPostalCode            | This field displays the postal code of the address for the contact associated with the given deal packet.                                                                                          |
| ContactRegion                | This field displays the region of the address for the contact associated with the given deal packet.                                                                                               |
| ContactTaxBody               | This field displays the tax body that the address for the contact associated with the given deal packet is located within.                                                                         |
| CurrencyCode                 | This field displays the currency code associated with the GL transaction for the given invoiced deal packet.                                                                                       |
| CustomerNumber               | This field displays the customer number of the customer associated with the given deal packet.                                                                                                     |
| CustomerPO                   | This field displays the purchase order number associated with the customer on the given deal packet.                                                                                               |
| DealContractDate             | This field displays the contract date of the deal that the given deal packet is associated with.                                                                                                   |
| DealNumber                   | This field displays the deal number of the deal that the given deal packet is associated with.                                                                                                     |
| DealPacketStatus             | This field displays the status of the given deal packet.                                                                                                                                           |
| DeliveryDate                 | This field displays the date on which the unit(s) associated with the given deal packet came into the possession of the customer.                                                                  |
| Department                   | This field displays the department associated with the given deal packet.                                                                                                                          |
| FinanceAmount                | This field displays the total amount of financing applied to particular units on the given deal packet.                                                                                            |
| FinanceCommission            | This field displays the total amount of finance commission on the given deal packet.                                                                                                               |
| FinanceReserve               | This field displays the total finance reserve amount associated with particular units on the given deal packet.                                                                                    |
| InsuranceCommission          | This field displays the total amount of insurance commission on the given deal packet.                                                                                                             |
| InsuranceIncome              | This field displays the total amount of insurance income on the given deal packet.                                                                                                                 |
| InvoiceDate                  | This field displays the date on which the given deal packet was invoiced.                                                                                                                          |
| InvoiceName1                 | This field displays the first name entered on the deal packet which should be printed on the invoice for the given deal packet.                                                                    |
| InvoiceName2                 | This field displays the second name entered on the deal packet which should be printed on the invoice for the given deal packet.                                                                   |
| InvoiceNumber                | This field displays the invoice number of the given invoiced deal packet.                                                                                                                          |
| InvoiceUser                  | This field displays the username of the user who invoiced the given invoiced deal packet.                                                                                                          |
| Journal                      | This field displays the journal which the GL transaction for the given deal packet is posted against.                                                                                              |
| JournalBranch                | This field displays the branch in which the journal entry for the GL transaction for the given deal packet was posted.                                                                             |
| JournalReference             | This field displays the reference number associated with the journal entry for the GL transaction for the given deal packet.                                                                       |
| LastUpdate                   | This field displays the date on which the given deal packet was last updated in the system.                                                                                                        |
| LastUpdateUser               | This field displays the username of the user who last updated the given deal packet in the system.                                                                                                 |
| OverrideExchangeRate         | This field displays the override exchange rate entered at the time of the GL transaction for the given deal packet.                                                                                |
| PacketNumber                 | This field displays the packet number of the given deal packet.                                                                                                                                    |
| PaymentMethod                | This field displays the payment method used by the customer on the given deal packet.                                                                                                              |
| PostDate                     | This field displays the date on which the GL transaction for the given deal packet was posted.                                                                                                     |
| PostPeriod                   | This field displays the month and year in which the GL transaction for the given deal packet was posted.                                                                                           |
| PostedAfterSalesCommission   | This field displays the total commission amount that was entered after the given deal packet was closed and posted to accounting.                                                                  |
| PostedAfterSalesExpense      | This field displays the total amount of expenses that were entered after the given deal packet was closed and posted to accounting.                                                                |
| SalesType                    | This field displays the sale type of the given deal packet.                                                                                                                                        |
| Salesperson                  | This field displays the username of the unit salesperson associated with the customer on the given deal packet.                                                                                    |
| ShipToAddress1               | This field displays the first line of the ship to address for the given deal packet.                                                                                                               |
| ShipToAddress2               | This field displays the second line of the ship to address for the given deal packet.                                                                                                              |
| ShipToCity                   | This field displays the city of the ship to address for the given deal packet.                                                                                                                     |
| ShipToCountry                | This field displays the country of the ship to address for the given deal packet.                                                                                                                  |
| ShipToCounty                 | This field displays the county of the ship to address for the given deal packet.                                                                                                                   |
| ShipToPostalCode             | This field displays the postal code of the ship to address for the given deal packet.                                                                                                              |
| ShipToRegion                 | This field displays the region of the ship to address for the given deal packet.                                                                                                                   |
| ShipToTaxBody                | This field displays the tax body that the ship to address for the given deal packet is located within.                                                                                             |
| SignDate                     | This field displays the date on which all of the documents for the given deal packet were signed by the customer.                                                                                  |
| TaxBasis                     | This field displays whether the sales tax on the given deal packet will be charged based on the local tax body or the tax body of the customer.                                                    |
| TaxBody                      | This field displays the overruling tax body of the given deal packet, from the Tax Information tab.                                                                                                |
| TaxRegion                    | This field displays the region associated with the tax body of the given deal packet.                                                                                                              |
| TaxStatus                    | This field displays the tax status of the given deal packet.                                                                                                                                       |
| TotalActualCashValue         | This field displays the total actual cash value of all trade in units on the given deal packet.                                                                                                    |
| TotalDealAddOnCost           | This field displays the total cost of all deal add ons on the given deal packet.                                                                                                                   |
| TotalDealAddOnPrice          | This field displays the total price of all deal add ons on the given deal packet.                                                                                                                  |
| TotalDeposits                | This field displays the total amount of all deposits on the given deal packet.                                                                                                                     |
| TotalDownPayments            | This field displays the total amount of all down payments on the given deal packet.                                                                                                                |
| TotalFET                     | This field displays the total amount of all FET charges on the given deal packet.                                                                                                                  |
| TotalFinanceReserve          | This field displays the total finance reserve amount on the given deal packet.                                                                                                                     |
| TotalFinanced                | This field displays the total amount of financing on the given deal packet.                                                                                                                        |
| TotalNonProfitDealAddOnCost  | This field displays the total cost of all deal add ons on the given deal packet that are not included in the profit calculation for the deal packet.                                               |
| TotalNonProfitDealAddOnPrice | This field displays the total price of all deal add ons on the given deal packet that are not included in the profit calculation for the deal packet.                                              |
| TotalNonProfitUnitAddOnCost  | This field displays the total cost of all unit add ons on the given deal packet that are not included in the profit calculation for the deal packet.                                               |
| TotalNonProfitUnitAddOnPrice | This field displays the total price of all unit add ons on the given deal packet that are not included in the profit calculation for the deal packet.                                              |
| TotalPayoff                  | This field displays the total amount of all payoffs on the given deal packet.                                                                                                                      |
| TotalProfit                  | This field displays the amount of the total price of the deal packet that is profit (price - cost).                                                                                                |
| TotalProfitDealAddOnCost     | This field displays the total cost of all deal add ons on the given deal packet that are included in the profit calculation for the deal packet.                                                   |
| TotalProfitDealAddOnPrice    | This field displays the total price of all deal add ons on the given deal packet that are included in the profit calculation for the deal packet.                                                  |
| TotalProfitPercent           | This field displays the percentage of the total price of the deal packet that is profit.                                                                                                           |
| TotalProfitUnitAddOnCost     | This field displays the total cost of all unit add ons on the given deal packet that are included in the profit calculation for the deal packet.                                                   |
| TotalProfitUnitAddOnPrice    | This field displays the total price of all unit add ons on the given deal packet that are included in the profit calculation for the deal packet.                                                  |
| TotalSalesTax                | This field displays the total amount of sales tax on the given deal packet.                                                                                                                        |
| TotalTradeInAllowance        | This field displays the total allowance given on all trade in units on the given deal packet.                                                                                                      |
| TotalUnitAddOnCost           | This field displays the total cost of all unit add ons on the given deal packet.                                                                                                                   |
| TotalUnitAddOnPrice          | This field displays the total price of all unit add ons on the given deal packet.                                                                                                                  |
| TotalUnitCost                | This field displays the total cost of all units on the given deal packet.                                                                                                                          |
| TotalUnitPrice               | This field displays the total price of all units on the given deal packet.                                                                                                                         |
