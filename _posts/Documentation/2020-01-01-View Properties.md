---
layout: post
title: "View Properties"
icon: "icon-list-alt"
category: "Documentation"
type: "usage" comments: falsedescription: Data reference documentation for fields, field types, and size
---


Key - This is the external name which will be used in a Unity API call.

Type - This helps determine what type the underlying functionality is such as
"View" for the SQL SSR views.

Command - This is the actual internal name that will be called.

HasReturn - This is a True/False indicator to show if the underlying
functionality has return data for example from an RPC call.

ReturnType - This describes the data type of the return data for example from an
RPC call.

DefaultSort - This determines the default sorting to use if one is not provided
in the Unity call for example the output from calling a SQL SSR view.

DefaultPageSize - This is the number of rows to return if no page size was
provided in the Unity call.

MaxPageSize - This is the maximum number of rows that can be returned in the
Unity call.

Input - This is a list of the input variables to be used, each entry has a
property for the name and data type.

Output - This is a list of the output variables provided, each entry has a
property for the name and data type.

## Accounting GL



---



### AccountAllocation 
```sql
Key: AccountAllocation,  
Type: View,  
Command: vwAC_SSR_AccountAllocation,  
HasReturn: false,  
ReturnType:  
DefaultSort: AllocationName,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,
```


#### Output:
```sql
Name: AccountAllocationID, Type: int  
Name: AccountingAccountID, Type: int  
Name: AllocationName, Type: varchar(250)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: AllocationType, Type: varchar(50)  
Name: BasedOn, Type: varchar(24)  
Name: IsDistributeEvenly, Type: bit  
Name: AllocationBranch, Type: varchar(10)  
Name: AllocationDepartment, Type: varchar(10)  
Name: PercentAllocated, Type: decimal  
Name: BreakdownAccounts, Type: nvarchar(max)  
Name: GLAccount, Type: varchar(20)  
Name: AccountDescription, Type: varchar(100)  
Name: GLBranch, Type: varchar(10)  
Name: GLDepartment, Type: varchar(10)
```

---



### ChartofAccounts

Key: ChartofAccounts,  
Type: View,  
Command: vwAC_SSR_ChartofAccounts,  
HasReturn: false,  
ReturnType:  
DefaultSort: Account,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: AccountingAccountID, Type: int  
Name: AccountingChartID, Type: int  
Name: AccountAllocationID, Type: int  
Name: QuickListID, Type: int  
Name: Account, Type: varchar(20)  
Name: ShortDescription, Type: varchar(50)  
Name: LongDescription, Type: varchar(100)  
Name: Departmentalized, Type: bit  
Name: AccountingType, Type: varchar(20)  
Name: ControlType, Type: varchar(20)  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime  
Name: AccountingCategoryTypeID, Type: int  
Name: StandardPresentation, Type: char  
Name: Level1Category, Type: varchar(100)  
Name: Level1SortOrder, Type: int  
Name: Level2Category, Type: varchar(100)  
Name: Level2SortOrder, Type: bigint  
Name: Level3Category, Type: varchar(100)  
Name: Level3SortOrder, Type: bigint  
Name: Level4Category, Type: varchar(100)  
Name: Level4SortOrder, Type: bigint  
Name: Level5Category, Type: varchar(100)  
Name: Level5SortOrder, Type: bigint  
Name: Level6Category, Type: varchar(100)  
Name: Level6SortOrder, Type: bigint  
Name: DetailLevel, Type: int  
Name: AccountingCategory, Type: varchar(100)  
Name: InActive, Type: bit  
Name: AllocationName, Type: int


---



### GeneralLedgerBalance 

Key: GeneralLedgerBalance,  
Type: View,  
Command: vwAC_SSR_GeneralLedgerBalance,  
HasReturn: false,  
ReturnType:  
DefaultSort: GLNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: DepartmentNumericCode, Type: varchar(10)  
Name: Division, Type: varchar(10)  
Name: GLNumber, Type: varchar(20)  
Name: Description, Type: varchar(100)  
Name: AccountingCategory, Type: varchar(100)  
Name: AccountType, Type: varchar(20)  
Name: FiscalYear, Type: int  
Name: AccountingPeriodBeginningDate, Type: date  
Name: JanuaryActivity, Type: decimal  
Name: FebruaryActivity, Type: decimal  
Name: MarchActivity, Type: decimal  
Name: AprilActivity, Type: decimal  
Name: MayActivity, Type: decimal  
Name: JuneActivity, Type: decimal  
Name: JulyActivity, Type: decimal  
Name: AugustActivity, Type: decimal  
Name: SeptemberActivity, Type: decimal  
Name: OctoberActivity, Type: decimal  
Name: NovemberActivity, Type: decimal  
Name: DecemberActivity, Type: decimal  
Name: JanuaryPriorActivity, Type: decimal  
Name: FebruaryPriorActivity, Type: decimal  
Name: MarchPriorActivity, Type: decimal  
Name: AprilPriorActivity, Type: decimal  
Name: MayPriorActivity, Type: decimal  
Name: JunePriorActivity, Type: decimal  
Name: JulyPriorActivity, Type: decimal  
Name: AugustPriorActivity, Type: decimal  
Name: SeptemberPriorActivity, Type: decimal  
Name: OctoberPriorActivity, Type: decimal  
Name: NovemberPriorActivity, Type: decimal  
Name: DecemberPriorActivity, Type: decimal  
Name: JanuaryBudget, Type: decimal  
Name: FebruaryBudget, Type: decimal  
Name: MarchBudget, Type: decimal  
Name: AprilBudget, Type: decimal  
Name: MayBudget, Type: decimal  
Name: JuneBudget, Type: decimal  
Name: JulyBudget, Type: decimal  
Name: AugustBudget, Type: decimal  
Name: SeptemberBudget, Type: decimal  
Name: OctoberBudget, Type: decimal  
Name: NovemberBudget, Type: decimal  
Name: DecemberBudget, Type: decimal  
Name: BalanceForward, Type: decimal  
Name: BalanceForwardPriorYear, Type: decimal  
Name: MTDActivity, Type: decimal  
Name: YTDActivity, Type: decimal  
Name: MTDActivityPriorYear, Type: decimal  
Name: YTDActivityPriorYear, Type: decimal  
Name: MTDBudget, Type: decimal  
Name: YTDBudget, Type: decimal  
Name: MTDActivityVariance, Type: decimal  
Name: YTDActivityVariance, Type: decimal  
Name: MTDBudgetVariance, Type: decimal  
Name: YTDBudgetVariance, Type: decimal


---



### GeneralLedgerTrans 

Key: GeneralLedgerTrans,  
Type: View,  
Command: vwAC_SSR_GeneralLedgerTrans,  
HasReturn: false,  
ReturnType:  
DefaultSort: GLAccount,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: AccountingAccountID, Type: int  
Name: APVendorID, Type: int  
Name: CustomerID, Type: int  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: DepartmentID, Type: int  
Name: NumericCode, Type: varchar(10)  
Name: GLAccount, Type: varchar(20)  
Name: GLDescription, Type: varchar(100)  
Name: FiscalYear, Type: int  
Name: AccountType, Type: varchar(20)  
Name: TransactionDescription, Type: varchar(50)  
Name: PostDate, Type: datetime  
Name: PostYear, Type: int  
Name: PostMonth, Type: int  
Name: PostingPeriod, Type: varchar(7)  
Name: OrderBranch, Type: varchar(100)  
Name: CheckNumber, Type: varchar(35)  
Name: PostingSequence, Type: int  
Name: Amount, Type: decimal  
Name: JournalReference, Type: varchar(250)  
Name: CustomerNumber, Type: varchar(10)  
Name: BranchDescription, Type: varchar(100)  
Name: Control, Type: varchar(50)  
Name: CustomerName, Type: varchar(100)  
Name: DaysOld, Type: int  
Name: DepartmentType, Type: varchar(50)  
Name: Journal, Type: varchar(50)  
Name: OverridePostingDescription, Type: varchar(250)  
Name: PostingDescription, Type: varchar(250)  
Name: IsReconciled, Type: bit  
Name: SourceApplication, Type: varchar(75)  
Name: TransactionDate, Type: datetime  
Name: User, Type: varchar(20)  
Name: Vendor, Type: varchar(100)  
Name: CompanyName, Type: varchar(100)  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: AccountingPeriodID, Type: int  
Name: AccountingPeriod, Type: int

## Accounting Payables



---



### APDetail 

Key: APDetail,  
Type: View,  
Command: vwAC_SSR_APDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: APInvoice,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: APInvoiceID, Type: int  
Name: GLJournalID, Type: int  
Name: APInvoice, Type: varchar(250)  
Name: PostingDescription, Type: varchar(250)  
Name: APInvoiceSource, Type: varchar(50)  
Name: BranchID, Type: int  
Name: Status, Type: varchar(20)  
Name: AddUserLoginID, Type: int  
Name: AddUserID, Type: int  
Name: UpdateUserID, Type: int  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: IsVoided, Type: bit  
Name: IsReversed, Type: bit  
Name: OriginalAPInvoiceID, Type: int  
Name: PostingDate, Type: datetime  
Name: AccountingPeriodID, Type: int  
Name: APVendorID, Type: int  
Name: InvoiceDate, Type: datetime  
Name: PaymentTermID, Type: int  
Name: NetDueDate, Type: datetime  
Name: InvoiceAmount, Type: decimal  
Name: SourceApplicationID, Type: int  
Name: DiscountDueDate, Type: datetime  
Name: DiscountAmount, Type: decimal  
Name: IsSuspended, Type: bit  
Name: SuspendedUserID, Type: int  
Name: ReleasedUserID, Type: int  
Name: SuspendedDate, Type: datetime  
Name: ReleasedDate, Type: datetime  
Name: PayeeName, Type: varchar(50)  
Name: PayeeAddressID, Type: int  
Name: EntityID, Type: int  
Name: ReferenceBranchID, Type: int  
Name: PostingReference, Type: varchar(50)  
Name: PaymentTerm, Type: varchar(50)  
Name: Vendor, Type: varchar(10)  
Name: VendorName, Type: varchar(100)  
Name: LastAmountPaid, Type: money  
Name: DateLastPaid, Type: datetime  
Name: AgeCategoryFromInvoiceDueDate, Type: varchar(12)  
Name: AgeCategoryFromInvoiceDate, Type: varchar(12)  
Name: ReferenceType, Type: varchar(28)  
Name: PostingBranch, Type: varchar(10)  
Name: ReferenceBranch, Type: varchar(10)  
Name: Balance, Type: decimal  
Name: PostingPeriod, Type: varchar(7)  
Name: Journal, Type: varchar(50)  
Name: VoidedDate, Type: datetime  
Name: VoidedUser, Type: varchar(20)  
Name: SuspendedUser, Type: varchar(20)  
Name: GLPostingSequence, Type: int  
Name: PaymentPostingSequence, Type: int  
Name: ReleasedUser, Type: varchar(20)  
Name: Bank, Type: varchar(20)  
Name: CheckNumber, Type: varchar(35)  
Name: CheckDate, Type: datetime  
Name: CheckAmount, Type: decimal  
Name: PaymentUser, Type: varchar(20)  
Name: PaymentVoidedUser, Type: varchar(20)  
Name: PayeeAddress1, Type: varchar(100)  
Name: PayeeAddress2, Type: varchar(100)  
Name: PayeeCity, Type: varchar(100)  
Name: PayeeRegion, Type: varchar(50)  
Name: PayeePostalCode, Type: varchar(15)  
Name: PayeeCountry, Type: varchar(35)  
Name: PayeeCounty, Type: varchar(35)  
Name: PaymentPostingBranch, Type: varchar(10)  
Name: IncomeType, Type: varchar(50)


---



### APGLDetail 

Key: APGLDetail,  
Type: View,  
Command: vwAC_SSR_APGLDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: APInvoice,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: APInvoice, Type: varchar(250)  
Name: APInvoiceID, Type: int  
Name: APInvoiceItemID, Type: int  
Name: PostingDescription, Type: varchar(250)  
Name: APVendorID, Type: int  
Name: Vendor, Type: varchar(10)  
Name: VendorName, Type: varchar(100)  
Name: PostingBranch, Type: varchar(10)  
Name: InvoiceDate, Type: datetime  
Name: InvoiceAmount, Type: decimal  
Name: GLAccount, Type: varchar(20)  
Name: GLBranch, Type: varchar(10)  
Name: Department, Type: varchar(100)  
Name: DebitAmount, Type: decimal  
Name: CreditAmount, Type: decimal  
Name: OverridePostingDescription, Type: varchar(250)  
Name: ControlValue, Type: varchar(50)  
Name: AllocationName, Type: varchar(250)  
Name: AccountingAccountID, Type: int


---



### APVendor 

Key: APVendor,  
Type: View,  
Command: vwAC_SSR_APVendor,  
HasReturn: false,  
ReturnType:  
DefaultSort: APVendor,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: APVendorID, Type: int  
  Name: APVendor, Type: varchar(10)  
  Name: CompanyName, Type: varchar(100)  
  Name: QuickLookup, Type: varchar(25)  
  Name: IsMiscellaneousAccount, Type: bit  
  Name: EstablishedDate, Type: datetime  
  Name: PaymentTerms, Type: varchar(50)  
  Name: APGroup, Type: varchar(50)  
  Name: CurrencyCode, Type: varchar(10)  
  Name: TaxpayerIdentificationNumber, Type: varchar(100)  
  Name: Is1099Required, Type: bit  
  Name: Inactive, Type: bit  
  Name: ControlBranchID, Type: int  
  Name: ControlBranch, Type: varchar(10)  
  Name: Address1, Type: varchar(100)  
  Name: Address2, Type: varchar(100)  
  Name: City, Type: varchar(100)  
  Name: Region, Type: varchar(6)  
  Name: PostalCode, Type: varchar(15)  
  Name: PhysicalCounty, Type: varchar(35)  
  Name: PhysicalCountry, Type: varchar(35)  
  Name: OfficePhone, Type: varchar(30)  
  Name: ShopPhone, Type: varchar(30)  
  Name: CellPhone, Type: varchar(30)  
  Name: Fax, Type: varchar(30)  
  Name: Email, Type: varchar(100)  
  Name: PhysicalContactName, Type: varchar(201)  
  Name: RemitToAddress1, Type: varchar(100)  
  Name: RemitToAddress2, Type: varchar(100)  
  Name: RemitToCity, Type: varchar(100)  
  Name: RemitToRegion, Type: varchar(6)  
  Name: RemitToPostalCode, Type: varchar(15)  
  Name: RemitToCounty, Type: varchar(35)  
  Name: RemitToCountry, Type: varchar(35)  
  Name: RemitToOfficePhone, Type: varchar(30)  
  Name: RemitToShopPhone, Type: varchar(30)  
  Name: RemitToCellPhone, Type: varchar(30)  
  Name: RemitToFax, Type: varchar(30)  
  Name: RemitToEmail, Type: varchar(100)  
  Name: RemitToContactName, Type: varchar(201)  
  Name: RemitToAllowEmail, Type: bit  
  Name: ShipToAddress1, Type: varchar(100)  
  Name: ShipToAddress2, Type: varchar(100)  
  Name: ShipToCity, Type: varchar(100)  
  Name: ShipToRegion, Type: varchar(6)  
  Name: ShipToPostalCode, Type: varchar(15)  
  Name: ShipToCounty, Type: varchar(35)  
  Name: ShipToCountry, Type: varchar(35)  
  Name: ShipToOfficePhone, Type: varchar(30)  
  Name: ShipToShopPhone, Type: varchar(30)  
  Name: ShipToCellPhone, Type: varchar(30)  
  Name: ShipToFax, Type: varchar(30)  
  Name: ShipToEmail, Type: varchar(100)  
  Name: ShipToContactName, Type: varchar(201)  
  Name: ShipToAllowEmail, Type: bit  
  Name: AmountNotDue, Type: decimal  
  Name: AmountDueNow, Type: decimal  
  Name: AmountDue30, Type: decimal  
  Name: AmountDue60, Type: decimal  
  Name: AmountDue90, Type: decimal  
  Name: AmountDueOver120, Type: decimal  
  Name: TotalAmount, Type: decimal  
  Name: InvoiceDateAmountNotDue, Type: decimal  
  Name: InvoiceDateAmountDueNow, Type: decimal  
  Name: InvoiceDateAmountDue30, Type: decimal  
  Name: InvoiceDateAmountDue60, Type: decimal  
  Name: InvoiceDateAmountDue90, Type: decimal  
  Name: InvoiceDateAmountDueOver120, Type: decimal  
  Name: DateLastPaid, Type: datetime  
  Name: LastAmountPaid, Type: decimal  
  Name: PaidYTD, Type: decimal  
  Name: PurchasesYTD, Type: decimal  
  Name: PaidPreviousYTD, Type: decimal  
  Name: PurchasesPreviousYTD, Type: decimal  
  Name: VendorComment, Type: nvarchar(max)  
  Name: AddDate, Type: datetime  
  Name: AddUser, Type: varchar(20)  
  Name: LastUpdateDate, Type: datetime  
  Name: LastUpdateUser, Type: varchar(20)  
  Name: LegalName, Type: varchar(100)  
  Name: RemitToName, Type: varchar(100)  
  Name: IncomeType, Type: varchar(50)


---



### MiscPODetail 

Key: MiscPODetail,  
Type: View,  
Command: vwAC_SSR_MiscPODetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: MPOHeaderID,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: MPODetailID, Type: int  
Name: MPOHeaderID, Type: int  
Name: Quantity, Type: int  
Name: UnitOfMeasure, Type: varchar(10)  
Name: PartVendor, Type: varchar(20)  
Name: PartNumber, Type: varchar(50)  
Name: PartDescription, Type: varchar(26)  
Name: PartPrice, Type: decimal  
Name: ExtendedPrice, Type: decimal  
Name: MiscellaneousChargeID, Type: int  
Name: IsDetailItem, Type: bit  
Name: MPOItemTypeID, Type: int  
Name: BillingReference, Type: varchar(100)  
Name: AddUserID, Type: int  
Name: UpdateUserID, Type: int  
Name: MPOItemSequence, Type: int  
Name: SupplierID, Type: int  
Name: POCodeID, Type: int  
Name: POBranchID, Type: int  
Name: BranchID, Type: int  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: MPODate, Type: datetime  
Name: PostDate, Type: datetime  
Name: BillingDate, Type: datetime  
Name: DepartmentID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: OrderNumber, Type: int  
Name: OrderStatus, Type: varchar(50)  
Name: Supplier, Type: varchar(20)  
Name: ItemType, Type: varchar(50)  
Name: OrderQuantity, Type: int  
Name: OrderExtPrice, Type: decimal  
Name: OrderPrice, Type: decimal  
Name: OrderCost, Type: decimal  
Name: OrderExtCost, Type: decimal  
Name: CustomerKey, Type: varchar(10)  
Name: MPOType, Type: varchar(20)  
Name: BillingStatus, Type: varchar(50)  
Name: VendorName, Type: varchar(100)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: ItemCostDifference, Type: decimal  
Name: TotalCostDifference, Type: decimal  
Name: ItemExtCostDifference, Type: decimal  
Name: POCode, Type: varchar(10)  
Name: POCodeDescription, Type: varchar(50)  
Name: BillableType, Type: varchar(12)


---



### MiscPOHeader 

Key: MiscPOHeader,  
Type: View,  
Command: vwAC_SSR_MiscPOHeader,  
HasReturn: false,  
ReturnType:  
DefaultSort: PONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: MPOHeaderID, Type: int  
Name: PONumber, Type: varchar(9)  
Name: MPOSequence, Type: varchar(2)  
Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: MPODate, Type: datetime  
Name: APVendor, Type: varchar(10)  
Name: ToName, Type: varchar(100)  
Name: MPOShippingTypeID, Type: int  
Name: ShipInstructions1, Type: varchar(20)  
Name: ShipInstructions2, Type: varchar(20)  
Name: MPOIsFor, Type: varchar(30)  
Name: Total, Type: decimal  
Name: IsBillable, Type: bit  
Name: MPOBillingStatusID, Type: int  
Name: MPOBillTypeID, Type: int  
Name: BillingCustomerID, Type: int  
Name: BillingBranchID, Type: int  
Name: BillingAmount, Type: decimal  
Name: BillingCost, Type: decimal  
Name: BillingInvoiceNumber, Type: varchar(50)  
Name: MPOControlNumber, Type: varchar(10)  
Name: IsManualChange, Type: bit  
Name: MPOLinkTypeID, Type: int  
Name: MPOLinkEntityID, Type: int  
Name: AddUserID, Type: int  
Name: UpdateUserID, Type: int  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: BillingDate, Type: datetime  
Name: CreatedBy, Type: varchar(20)  
Name: APVendorID, Type: int  
Name: TotalValue, Type: decimal  
Name: OrderNumber, Type: varchar(12)  
Name: BillableType, Type: varchar(12)  
Name: IsManuallyReferenced, Type: bit  
Name: VoidDate, Type: datetime  
Name: VoidUser, Type: varchar(20)  
Name: IsVoided, Type: bit


---



### NotesPayable 

Key: NotesPayable,  
Type: View,  
Command: vwAC_SSR_NotesPayable,  
HasReturn: false,  
ReturnType:  
DefaultSort: NoteNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: Branch, Type: varchar(10)  
Name: BranchName, Type: varchar(100)  
Name: BranchID, Type: int  
Name: Lender, Type: varchar(100)  
Name: NotesPayableID, Type: int  
Name: NoteNumber, Type: varchar(50)  
Name: Description, Type: varchar(100)  
Name: NoteType, Type: varchar(15)  
Name: NotesPayableGroup, Type: varchar(50)  
Name: Inactive, Type: bit  
Name: NoteDate, Type: datetime  
Name: MaturityDate, Type: datetime  
Name: FirstPaymentDate, Type: datetime  
Name: NextPaymentDate, Type: datetime  
Name: LastPaymentDate, Type: datetime  
Name: LastPayment, Type: decimal  
Name: InterestCalculationMethod, Type: int  
Name: PaidOff, Type: bit  
Name: TotalPrincipal, Type: decimal  
Name: InterestRate, Type: decimal  
Name: BalloonAmount, Type: decimal  
Name: BillingRateFrequency, Type: varchar(12)  
Name: Payment, Type: decimal  
Name: TotalInterest, Type: decimal  
Name: TotalPayments, Type: int  
Name: PaidPrincipal, Type: decimal  
Name: PaidInterest, Type: decimal  
Name: PaymentsMade, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: BalloonMethod, Type: varchar(27)  
Name: DaysinYear, Type: varchar(8)  
Name: Is1099Required, Type: bit


---



### NotesPayableDetail 

Key: NotesPayableDetail,  
Type: View,  
Command: vwAC_SSR_NotesPayableDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: NoteNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: NotesPayableDetailID, Type: int  
Name: NotesPayableID, Type: int  
Name: NoteNumber, Type: varchar(50)  
Name: Description, Type: varchar(100)  
Name: NoteType, Type: varchar(15)  
Name: UnitNumber, Type: varchar(20)  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: CONTROL, Type: varchar(20)  
Name: AllocationAmount, Type: decimal  
Name: AllocationPercentage, Type: decimal  
Name: OverrideNotesPayableGroup, Type: varchar(50)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: PaidInterest, Type: decimal  
Name: PaidPrincipal, Type: decimal  
Name: PaymentsMade, Type: int  
Name: PaidOff, Type: bit  
Name: LastPaymentDate, Type: datetime  
Name: LocationBranch, Type: varchar(10)  
Name: IncomeType, Type: varchar(50)

## Accounting Receiveables



---



### ARDetail 

Key: ARDetail,  
Type: View,  
Command: vwAC_SSR_ARDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: ID, Type: int  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: CustomerID, Type: int  
Name: AgeCategory, Type: varchar(12)  
Name: InvAgeCategory, Type: varchar(12)  
Name: InvoiceEntityTypeID, Type: int  
Name: InvoiceType, Type: varchar(32)  
Name: CreditLimit, Type: decimal  
Name: Amount, Type: decimal  
Name: PaidAmount, Type: decimal  
Name: InvoiceNumber, Type: varchar(100)  
Name: InvoiceDueDate, Type: datetime  
Name: BranchID, Type: int  
Name: BranchCode, Type: varchar(10)  
Name: DiscountAmount, Type: decimal  
Name: InvoiceDate, Type: datetime  
Name: DaysOld, Type: int  
Name: InvDaysOld, Type: int  
Name: PaymentMethod, Type: varchar(50)  
Name: PaymentTerm, Type: varchar(50)  
Name: PaymentTermID, Type: int  
Name: InvoiceID, Type: int  
Name: PaymentBalance, Type: decimal  
Name: PaymentMethodID, Type: int  
Name: CustomerPONumber, Type: varchar(50)  
Name: UserDefinedPaymentMethod, Type: varchar(50)  
Name: UserDefinedPaymentMethodID, Type: int  
Name: InvoiceDescription, Type: varchar(194)  
Name: OriginalDueDate, Type: datetime  
Name: OutSideSalesPerson, Type: varchar(50)  
Name: SeparateStatement, Type: int  
Name: CustomerParentID, Type: int  
Name: CustomerParentID_IgnoreStatementType, Type: int  
Name: InvoiceUser, Type: varchar(20)  
Name: GrossMargin, Type: decimal  
Name: InvoiceBalance, Type: decimal  
Name: Department, Type: varchar(100)  
Name: DepartmentID, Type: int  
Name: IsDisputeInvoice, Type: bit  
Name: NumberPayments, Type: int  
Name: CustomerBaseBranch, Type: varchar(10)


---



### Customer 

Key: Customer,  
Type: View,  
Command: vwAC_SSR_Customer,  
HasReturn: false,  
ReturnType:  
DefaultSort: CustomerKey,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: CustomerID, Type: int  
Name: BillToAddressID, Type: int  
Name: ShipToAddressID, Type: int  
Name: CustomerBaseBranchID, Type: int  
Name: BaseBranch, Type: varchar(10)  
Name: CustomerBaseBranchName, Type: varchar(100)  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: ControlBranchID, Type: int  
Name: ControlBranch, Type: varchar(10)  
Name: Inactive, Type: bit  
Name: IsProspect, Type: bit  
Name: IndustryTypeID, Type: int  
Name: BusinessStructureID, Type: int  
Name: BusinessStructure, Type: varchar(50)  
Name: BusinessTaxID, Type: varchar(20)  
Name: CurrencyCodeID, Type: int  
Name: CurrencyCode, Type: varchar(10)  
Name: MiscellaneousAccount, Type: bit  
Name: InternalAccount, Type: bit  
Name: WarrantyAccount, Type: bit  
Name: InternalLRCustomer, Type: bit  
Name: SubjectToFinanceCharge, Type: bit  
Name: PerformCreditCheck, Type: bit  
Name: Relationship, Type: varchar(6)  
Name: IsSeparateStatement, Type: int  
Name: InvoiceEmail, Type: varchar(100)  
Name: IsInvoiceEmailAllowed, Type: bit  
Name: StatementEmail, Type: varchar(100)  
Name: IsStatementEmailAllowed, Type: bit  
Name: AlertEmail, Type: varchar(100)  
Name: IsAlertEmailAllowed, Type: bit  
Name: PartsInvoiceEmail, Type: varchar(100)  
Name: IsPartsInvoiceEmailAllowed, Type: bit  
Name: RepairOrderInvoiceEmail, Type: varchar(100)  
Name: IsRepairOrderInvoiceEmailAllowed, Type: bit  
Name: SalesInvoiceEmail, Type: varchar(100)  
Name: IsSalesInvoiceEmailAllowed, Type: bit  
Name: LeaseRentalInvoiceEmail, Type: varchar(100)  
Name: IsLeaseRentalInvoiceEmailAllowed, Type: bit  
Name: FuelInvoiceEmail, Type: varchar(100)  
Name: IsFuelInvoiceEmailAllowed, Type: bit  
Name: IsQuickCreate, Type: bit  
Name: LastInvoiceDate, Type: datetime  
Name: LastPaymentDate, Type: datetime  
Name: InvoicesYTD, Type: int  
Name: InvoicesPYR, Type: int  
Name: HighOnAccountYTD, Type: decimal  
Name: HighOnAccountPYR, Type: decimal  
Name: PaymentsYTD, Type: int  
Name: PaymentsPYR, Type: int  
Name: AverageDaysToPayYTD, Type: int  
Name: AverageDaysToPayPYR, Type: int  
Name: StatementType, Type: varchar(20)  
Name: CustomerPartsServiceID, Type: int  
Name: PartsServiceCustomerContactID, Type: int  
Name: CustomerPartsServiceAccountStatusID, Type: int  
Name: AccountStatus, Type: varchar(50)  
Name: TaxCodeID, Type: int  
Name: TaxStatus, Type: varchar(50)  
Name: OutsidePartsSalesperson, Type: varchar(20)  
Name: OutsideServiceSalesperson, Type: varchar(50)  
Name: ServiceSalespersonID, Type: int  
Name: ServiceSalesperson, Type: varchar(20)  
Name: ServiceSalespersonName, Type: varchar(201)  
Name: Territory, Type: varchar(50)  
Name: AllowServiceUnitOwnership, Type: bit  
Name: IsLeaseRentalUnitRequired, Type: bit  
Name: QLLaborAccountingID, Type: int  
Name: LaborAccountingCode, Type: varchar(50)  
Name: QLPartsAccountingID, Type: int  
Name: PartsAccountingCode, Type: varchar(50)  
Name: PaymentTermID, Type: int  
Name: PaymentTerm, Type: varchar(50)  
Name: DefaultPaymentMethodID, Type: int  
Name: DefaultPaymentMethod, Type: varchar(50)  
Name: IsCustomerPORequired, Type: bit  
Name: IsEHCExempt, Type: bit  
Name: PartsServiceCreditLimit, Type: decimal  
Name: SeparateCoreInvoices, Type: bit  
Name: AlternateCoreCustomer, Type: varchar(10)  
Name: SeparateCoreStatements, Type: bit  
Name: SeparateCoreTerms, Type: varchar(50)  
Name: OutputSeparateCoreStatements, Type: bit  
Name: IsLPORequired, Type: bit  
Name: PickupDeliveryMethod, Type: varchar(100)  
Name: NoUsageUpdate, Type: bit  
Name: PrintPartLabelsForPartsInvoices, Type: bit  
Name: SurchargeExempt, Type: bit  
Name: SurchargeZone, Type: varchar(50)  
Name: BlanketPONumber, Type: varchar(30)  
Name: IgnoreAccountingGroup, Type: bit  
Name: PrintExportLabels, Type: bit  
Name: SalesManagementAccountStatus, Type: varchar(50)  
Name: SalesManagementTaxStatus, Type: varchar(50)  
Name: SalesManagementUserName, Type: varchar(20)  
Name: SalesManagementSalesmanNumber, Type: varchar(20)  
Name: SalesManagementSalesman, Type: varchar(201)  
Name: Established Date, Type: datetime  
Name: SalesManagementCustomerCreditLimit, Type: decimal  
Name: CustAddUserID, Type: int  
Name: CustAddUser, Type: varchar(20)  
Name: CustAddDate, Type: datetime  
Name: CustUpdateUserID, Type: int  
Name: CustUpdateUser, Type: varchar(20)  
Name: CustLastUpdate, Type: datetime  
Name: CustAddDateTimeZone, Type: decimal  
Name: CustLastUpdateTimeZone, Type: decimal  
Name: OutsidePartsSalespersonID, Type: int  
Name: TotalBalanceDue, Type: decimal  
Name: GrandTotalBalanceDue, Type: decimal  
Name: LastPayment, Type: decimal  
Name: IndustryType, Type: varchar(50)  
Name: Amount Due Now, Type: decimal  
Name: Amount Due 30, Type: decimal  
Name: Amount Due 60, Type: decimal  
Name: Amount Due 90, Type: decimal  
Name: Amount Due Over 120, Type: decimal  
Name: Amount Not Due, Type: decimal  
Name: Unapplied Cash, Type: decimal  
Name: Total Balance Due, Type: decimal  
Name: ParentCustomerNumber, Type: varchar(10)  
Name: ShopPhone, Type: varchar(30)  
Name: OfficePhone, Type: varchar(30)  
Name: CellPhone, Type: varchar(30)  
Name: Fax, Type: varchar(30)  
Name: BillToAddress1, Type: varchar(100)  
Name: BillToAddress2, Type: varchar(100)  
Name: BillToCity, Type: varchar(100)  
Name: BillToRegion, Type: varchar(6)  
Name: BillToTaxBody, Type: varchar(50)  
Name: BillToPostalCode, Type: varchar(15)  
Name: ShipToAddress1, Type: varchar(100)  
Name: ShipToAddress2, Type: varchar(100)  
Name: ShipToCity, Type: varchar(100)  
Name: ShipToRegion, Type: varchar(6)  
Name: ShipToTaxBody, Type: varchar(50)  
Name: ShipToPostalCode, Type: varchar(15)  
Name: CustomerPriceType, Type: varchar(50)  
Name: EntityTypeID, Type: int  
Name: BillToAddressTypeID, Type: int  
Name: ShipToAddressTypeID, Type: int  
Name: SubjectToDelinquency, Type: bit  
Name: OverrideDelinquencyTerms, Type: int  
Name: AllowFuelTicket, Type: bit  
Name: FuelOverridePaymentTerms, Type: varchar(50)  
Name: SeparateInvoicePetFuelTicket, Type: bit  
Name: NationaLeaseAccountNumber, Type: varchar(30)  
Name: LeaseContractSalesperson, Type: varchar(20)  
Name: RentalContractSalesperson, Type: varchar(20)  
Name: MaintenanceContractSalesperson, Type: varchar(20)  
Name: DOT, Type: varchar(100)  
Name: CVOR, Type: varchar(100)  
Name: CommentTablesID, Type: int  
Name: CanadianTaxID, Type: varchar(15)  
Name: QuebecTaxID, Type: varchar(16)  
Name: InvoiceDateAmountNotDue, Type: decimal  
Name: InvoiceDateAmountDueNow, Type: decimal  
Name: InvoiceDateAmountDue30, Type: decimal  
Name: InvoiceDateAmountDue60, Type: decimal  
Name: InvoiceDateAmountDue90, Type: decimal  
Name: InvoiceDateAmountDueOver120, Type: decimal  
Name: OverridePastDueDays, Type: int  
Name: IsPastDue, Type: bit  
Name: IsSubjectToPastDue, Type: bit  
Name: PastDueAmount, Type: decimal  
Name: TotalCreditReserve, Type: decimal


---



### CustomerMiscPrompt 

Key: CustomerMiscPrompt,  
Type: View,  
Command: vwAC_SSR_CustomerMiscPrompt,  
HasReturn: false,  
ReturnType:  
DefaultSort: [Customer Number],  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: Prompt, Type: varchar(20)  
Name: Description, Type: varchar(50)  
Name: Value, Type: varchar(50)  
Name: Customer Number, Type: varchar(10)  
Name: Company Name, Type: varchar(100)  
Name: CustomerID, Type: int


---



### InvoiceSalesSummary 

Key: InvoiceSalesSummary,  
Type: View,  
Command: vwAC_SSR_InvoiceSalesSummary,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsSalesOrderInvoiceID, Type: int  
Name: RepairOrderInvoiceID, Type: int  
Name: FinanceChargeInvoiceID, Type: int  
Name: AdjustmentInvoiceID, Type: int  
Name: LeaseContractInvoiceID, Type: int  
Name: DealPacketInvoiceID, Type: int  
Name: FuelInvoiceID, Type: int  
Name: InvoiceDetailJoinID, Type: int  
Name: InvoiceType, Type: varchar(19)  
Name: OrderType, Type: varchar(50)  
Name: DivisionID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: Department, Type: varchar(10)  
Name: DepartmentID, Type: int  
Name: InvoiceDate, Type: datetime  
Name: InvoiceNumber, Type: varchar(50)  
Name: OrderNumber, Type: varchar(31)  
Name: CustomerID, Type: int  
Name: Customer, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: BillingCustomerID, Type: int  
Name: BillingCustomer, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: CustomerPO, Type: varchar(50)  
Name: InvoiceUser, Type: varchar(20)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: IsVoidedInvoice, Type: bit  
Name: OrderCustomerAddress1, Type: varchar(100)  
Name: OrderCustomerAddress2, Type: varchar(100)  
Name: OrderCustomerCity, Type: varchar(100)  
Name: OrderCustomerCounty, Type: varchar(100)  
Name: OrderCustomerRegion, Type: varchar(6)  
Name: OrderCustomerPostalCode, Type: varchar(15)  
Name: BillingCustomerAddress1, Type: varchar(100)  
Name: BillingCustomerAddress2, Type: varchar(100)  
Name: BillingCustomerCity, Type: varchar(100)  
Name: BillingCustomerCounty, Type: varchar(100)  
Name: BillingCustomerRegion, Type: varchar(6)  
Name: BillingCustomerPostalCode, Type: varchar(15)  
Name: InvoiceSubTotal, Type: decimal  
Name: InvoiceTaxTotal, Type: decimal  
Name: InvoiceTotal, Type: decimal  
Name: TotalReplacementCost, Type: decimal  
Name: TotalAverageCost, Type: decimal  
Name: ReplacementCostGrossProfit, Type: decimal  
Name: AverageCostGrossProfit, Type: decimal  
Name: ReplacementCostGrossProfitMargin, Type: decimal  
Name: AverageCostGrossProfitMargin, Type: decimal  
Name: PaymentMethod, Type: varchar(50)  
Name: Salesperson, Type: varchar(50)  
Name: InvoiceYear, Type: varchar(4)  
Name: InvoiceMonth, Type: varchar(2)  
Name: IsLocal, Type: bit


---



### InvoiceSalesSummaryDetail 

Key: InvoiceSalesSummaryDetail,  
Type: View,  
Command: vwAC_SSR_InvoiceSalesSummaryDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsSalesOrderInvoiceID, Type: int  
Name: RepairOrderInvoiceID, Type: int  
Name: FinanceChargeInvoiceID, Type: int  
Name: AdjustmentInvoiceID, Type: int  
Name: LeaseContractInvoiceID, Type: int  
Name: DealPacketInvoiceID, Type: int  
Name: FuelInvoiceID, Type: int  
Name: InvoiceID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: UnitInventoryID, Type: int  
Name: BranchID, Type: int  
Name: InvoiceType, Type: varchar(32)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: InsideSalesperson, Type: varchar(50)  
Name: OutsideSalesperson, Type: varchar(50)  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(100)  
Name: Department, Type: varchar(100)  
Name: OrderNumber, Type: int  
Name: OrderStatus, Type: varchar(50)  
Name: TaskNumber, Type: smallint  
Name: InvoiceDate, Type: datetime  
Name: InvoiceNumber, Type: varchar(53)  
Name: CustomerID, Type: int  
Name: Customer, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: BillingCustomerID, Type: int  
Name: BillingCustomer, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: UnitNumber, Type: varchar(20)  
Name: StockNumber, Type: varchar(20)  
Name: ItemType, Type: varchar(50)  
Name: Supplier, Type: varchar(50)  
Name: Item, Type: varchar(100)  
Name: PartType, Type: varchar(4)  
Name: ItemDescription, Type: varchar(203)  
Name: BillingRateFrequency, Type: varchar(25)  
Name: MeterType, Type: varchar(25)  
Name: Quantity, Type: decimal  
Name: PartsActionType, Type: varchar(50)  
Name: AverageCost, Type: money  
Name: ReplacementCost, Type: money  
Name: ExtendedAverageCost, Type: money  
Name: ExtendedReplacementCost, Type: money  
Name: CalculatedPrice, Type: money  
Name: OverridePrice, Type: decimal  
Name: Price, Type: money  
Name: ExtendedPrice, Type: money  
Name: OEMPrice, Type: money  
Name: OEMRebateAmount, Type: money  
Name: IsBillingAdjustment, Type: bit  
Name: OTHours, Type: decimal  
Name: OTMultiplier, Type: decimal  
Name: IsBillCustomerOT, Type: bit  
Name: AverageCostGrossProfit, Type: money  
Name: AverageCostGrossProfitMargin, Type: money  
Name: ReplacementCostGrossProfit, Type: money  
Name: ReplacementCostGrossProfitMargin, Type: money

## Accounting Other



---



### Address 

Key: Address,  
Type: View,  
Command: vwAC_SSR_Address,  
HasReturn: false,  
ReturnType:  
DefaultSort: City,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: AddressID, Type: int  
Name: AddressTypeID, Type: int  
Name: AddressType, Type: varchar(50)  
Name: EntityTypeID, Type: int  
Name: EntityType, Type: varchar(50)  
Name: EntityID, Type: int  
Name: ContactID, Type: int  
Name: IsPrimary, Type: bit  
Name: Street1, Type: varchar(100)  
Name: Street2, Type: varchar(100)  
Name: City, Type: varchar(100)  
Name: RegionID, Type: int  
Name: Region, Type: varchar(6)  
Name: PostalCode, Type: varchar(15)  
Name: Country, Type: varchar(35)  
Name: County, Type: varchar(35)  
Name: TaxBodyID, Type: int  
Name: TaxBody, Type: varchar(50)  
Name: Inactive, Type: bit  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDateTime, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateTime, Type: datetime  
Name: SalesPersonID, Type: int  
Name: Salesperson, Type: varchar(20)  
Name: Territory, Type: varchar(50)


---



### CheckRegister

Key: CheckRegister,  
Type: View,  
Command: vwAC_SSR_CheckRegister,  
HasReturn: false,  
ReturnType:  
DefaultSort: CheckNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PostingBranch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: Bank, Type: varchar(20)  
Name: CheckNumber, Type: varchar(35)  
Name: CheckDate, Type: datetime  
Name: CheckAmount, Type: decimal  
Name: APVendorID, Type: int  
Name: APVendor, Type: varchar(10)  
Name: CustomerID, Type: int  
Name: CustomerNumber, Type: varchar(10)  
Name: LenderID, Type: int  
Name: Lender, Type: varchar(100)  
Name: PayeeName, Type: varchar(50)  
Name: Address1, Type: varchar(100)  
Name: Address2, Type: varchar(100)  
Name: City, Type: varchar(100)  
Name: PostalCode, Type: varchar(15)  
Name: Region, Type: varchar(6)  
Name: PostingPeriod, Type: varchar(7)  
Name: PostingSequence, Type: int  
Name: SourceEntityID, Type: int  
Name: APCheckProcessingID, Type: int  
Name: CheckRegisterID, Type: int  
Name: CheckSource, Type: varchar(31)  
Name: CheckStatus, Type: varchar(10)  
Name: VoidDate, Type: datetime  
Name: IsVoided, Type: bit  
Name: VoidUser, Type: varchar(20)  
Name: VoidDescription, Type: varchar(100)  
Name: VoidPostingSequence, Type: varchar(50)  
Name: VoidPeriod, Type: varchar(7)  
Name: ClearedStatus, Type: varchar(11)  
Name: Cleared, Type: bit  
Name: ClearedDate, Type: date  
Name: IsReconciled, Type: bit  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: Is1099Required, Type: bit  
Name: IncomeType, Type: varchar(50)


---



### Comments 

Key: Comments,  
Type: View,  
Command: vwAC_SSR_Comments,  
HasReturn: false,  
ReturnType:  
DefaultSort: AddDate,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: CommentID, Type: int  
Name: EntityID, Type: int  
Name: CommentTablesID, Type: int  
Name: CommentTable, Type: varchar(50)  
Name: CommentTableDescription, Type: varchar(50)  
Name: CommentTypeID, Type: int  
Name: CommentType, Type: varchar(10)  
Name: CommentTypeDescription, Type: varchar(50)  
Name: BriefDescription, Type: varchar(50)  
Name: Comment, Type: varchar(7500)  
Name: Posted, Type: bit  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)


---



### FixedAssets 

Key: FixedAssets,  
Type: View,  
Command: vwAC_SSR_FixedAssets,  
HasReturn: false,  
ReturnType:  
DefaultSort: Description,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BookBranch, Type: varchar(10)  
Name: LocationBranch, Type: varchar(25)  
Name: Asset, Type: varchar(50)  
Name: Description, Type: varchar(100)  
Name: AcquisitionCost, Type: decimal  
Name: MonthlyDepreciation, Type: decimal  
Name: AccumulatedDepreciation, Type: decimal  
Name: CurrentValue, Type: decimal  
Name: InServiceDate, Type: datetime  
Name: MfgSerialNumber, Type: varchar(25)  
Name: Category, Type: varchar(50)  
Name: DisposalDate, Type: datetime  
Name: DisposalValue, Type: decimal  
Name: EstimatedLifeMos, Type: int  
Name: EstimatedLifeDate, Type: datetime  
Name: AcquisitionDate, Type: datetime  
Name: UsedLifeMonths, Type: int  
Name: RemainLifeMonths, Type: int  
Name: Type, Type: varchar(4)  
Name: Method, Type: varchar(50)  
Name: ResidualValue, Type: decimal  
Name: PostingPeriod, Type: datetime  
Name: PostDate, Type: datetime  
Name: MinRemainLifeMonths, Type: int  
Name: AllocationName, Type: varchar(250)  
Name: ExtendAssetLife, Type: int  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: YTDDepreciation, Type: decimal  
Name: Inactive, Type: bit


---



### SalesPersonCommission 

Key: SalesPersonCommission,  
Type: View,  
Command: vwAC_SSR_SalesPersonCommission,  
HasReturn: false,  
ReturnType:  
DefaultSort: Salesperson,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: CommissionTable, Type: varchar(50)  
Name: Salesperson, Type: varchar(20)  
Name: SalespersonName, Type: varchar(201)  
Name: Branch, Type: varchar(100)  
Name: Department, Type: varchar(10)  
Name: Item, Type: varchar(100)  
Name: InvoiceNumber, Type: varchar(50)  
Name: Customer, Type: varchar(100)  
Name: ExtendedPrice, Type: decimal  
Name: ExtendedCost, Type: decimal  
Name: Quantity, Type: decimal  
Name: GrossProfitMargin, Type: decimal  
Name: GrossProfit, Type: decimal  
Name: Commission, Type: decimal  
Name: Commission Rate, Type: decimal  
Name: InvoiceDateandTime, Type: datetime  
Name: InvoiceDate, Type: datetime  
Name: IsOutsideSalesperson, Type: varchar(3)  
Name: IsVoided, Type: varchar(3)

## Lease/Rental



---



### CustomerInsurance 

Key: CustomerInsurance,  
Type: View,  
Command: vwLR_SSR_CustomerInsurance,  
HasReturn: false,  
ReturnType:  
DefaultSort: CustomerNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: CustomerInsuranceID, Type: int  
Name: CustomerNumber, Type: varchar(10)  
Name: CustomerID, Type: int  
Name: CompanyName, Type: varchar(100)  
Name: PolicyNumber, Type: varchar(100)  
Name: Description, Type: varchar(30)  
Name: InsuranceProvider, Type: varchar(100)  
Name: AgentName, Type: varchar(100)  
Name: ExpirationDate, Type: datetime  
Name: OfficePhone, Type: varchar(30)  
Name: Fax, Type: int  
Name: Address1, Type: varchar(100)  
Name: Address2, Type: varchar(100)  
Name: City, Type: varchar(100)  
Name: Region, Type: varchar(6)  
Name: PostalCode, Type: varchar(15)  
Name: LiablityCoverage, Type: decimal  
Name: LiablityDeductible, Type: decimal  
Name: DamageCollisionCoverage, Type: decimal  
Name: DamageCollisionDeductible, Type: decimal  
Name: DamageComprehensiveCoverage, Type: decimal  
Name: DamageComprehensiveDeductible, Type: decimal  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime  
Name: Email, Type: varchar(100)  
Name: StartDate, Type: datetime  
Name: ProviderType, Type: varchar(50)  
Name: IsCompanyProvidedInsurance, Type: bit  
Name: PhysicalDamageCoverageLimit, Type: decimal  
Name: Inactive, Type: bit


---



### DriverInfo 

Key: DriverInfo,  
Type: View,  
Command: vwLR_SSR_DriverInfo,  
HasReturn: false,  
ReturnType:  
DefaultSort: CustomerKey,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: DriverLicenseID, Type: int  
Name: CustomerID, Type: int  
Name: LicenseNumber, Type: varchar(50)  
Name: Region, Type: varchar(6)  
Name: ExpirationDate, Type: datetime  
Name: Type, Type: varchar(100)  
Name: DateOfBirth, Type: datetime  
Name: Inactive, Type: bit  
Name: AddUserID, Type: int  
Name: AddUserName, Type: varchar(20)  
Name: UpdateUserID, Type: int  
Name: UpdateUserName, Type: varchar(20)  
Name: FirstName, Type: varchar(100)  
Name: LastName, Type: varchar(100)  
Name: MiddleInitial, Type: char  
Name: WorkPhone, Type: varchar(30)  
Name: DriverName, Type: varchar(201)  
Name: Street1, Type: varchar(100)  
Name: Street2, Type: varchar(100)  
Name: City, Type: varchar(100)  
Name: PostalCode, Type: varchar(15)  
Name: Country, Type: varchar(35)  
Name: County, Type: varchar(35)  
Name: Region1, Type: varchar(6)  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime


---



### LRBillingGroup 

Key: LRBillingGroup,  
Type: View,  
Command: vwLR_SSR_LRBillingGroup,  
HasReturn: false,  
ReturnType:  
DefaultSort: NAME,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseRentalBillingGroupID, Type: int  
Name: NAME, Type: varchar(50)  
Name: BillingCycleType, Type: varchar(22)  
Name: BillingCycleFrequency, Type: varchar(50)  
Name: LastBilledDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: GroupBillingCycle, Type: int  
Name: DailyBilling, Type: int  
Name: DailyBillingCycle, Type: int


---



### LRBillingHistoryHeader 

Key: LRBillingHistoryHeader,  
Type: View,  
Command: vwLR_SSR_LRBillingHistoryHeader,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseContractInvoiceID, Type: int  
Name: CustomerID, Type: int  
Name: LeasceContractID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(100)  
Name: Department, Type: varchar(100)  
Name: InvoiceNumber, Type: varchar(50)  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: FixedBillingGroup, Type: varchar(50)  
Name: VariableBillingGroup, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: PostingPeriod, Type: varchar(33)  
Name: ContractNumber, Type: int  
Name: PaymentMethod, Type: varchar(50)  
Name: PaymentTerms, Type: varchar(50)  
Name: DueDate, Type: datetime  
Name: TotalFixed, Type: decimal  
Name: TotalVariable, Type: decimal  
Name: TotalMisc, Type: decimal  
Name: Subtotal, Type: decimal  
Name: TotalTax, Type: decimal  
Name: TotalInvoice, Type: decimal  
Name: IsVoided, Type: bit  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: ContractSalesperson, Type: varchar(50)  
Name: ContractPO, Type: varchar(50)  
Name: FixedChargesPO, Type: varchar(50)  
Name: VariableChargesPO, Type: varchar(50)  
Name: MiscChargesPO, Type: varchar(50)


---



### LRBillingHistoryDetail 

Key: LRBillingHistoryDetail,  
Type: View,  
Command: vwLR_SSR_LRBillingHistoryDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseContractUnitID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(100)  
Name: BranchID, Type: int  
Name: Department, Type: varchar(100)  
Name: ContractNumber, Type: int  
Name: Status, Type: varchar(8)  
Name: InvoiceDate, Type: datetime  
Name: LeaseContractUnitInvoiceID, Type: int  
Name: LeaseContractInvoiceID, Type: int  
Name: InvoiceNumber, Type: varchar(50)  
Name: ChargeType, Type: varchar(25)  
Name: Charge, Type: varchar(25)  
Name: ChargeDescription, Type: varchar(100)  
Name: Quantity, Type: decimal  
Name: Cost, Type: decimal  
Name: Rate, Type: decimal  
Name: ExtendedCost, Type: decimal  
Name: ExtendedRate, Type: decimal  
Name: BillingRateFrequency, Type: varchar(25)  
Name: MeterType, Type: varchar(25)  
Name: UnitStatus, Type: varchar(50)  
Name: LeaseContractChargeInvoiceID, Type: int  
Name: UnitNumber, Type: varchar(20)  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: IsVoided, Type: bit  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: StockNumber, Type: varchar(20)  
Name: UnitInventoryID, Type: int  
Name: ContractSalesperson, Type: varchar(50)  
Name: UnitSalesperson, Type: varchar(20)


---



### LRBillingHistory 

Key: LRBillingHistory,  
Type: View,  
Command: vwLR_SSR_LRBillingHistory,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeasceContractID, Type: int  
Name: LeaseContractInvoiceID, Type: int  
Name: LeaseContractUnitID, Type: int  
Name: UnitInventoryID, Type: int  
Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: CustomerID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: InvoiceNumber, Type: varchar(50)  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: FixedChargeBillingGroup, Type: varchar(50)  
Name: VariableChargeBillingGroup, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: PostingPeriod, Type: varchar(33)  
Name: IsVoided, Type: bit  
Name: ContractNumber, Type: int  
Name: FixedChargeStartDate, Type: datetime  
Name: FixedChargeEndDate, Type: datetime  
Name: VariableChargeStartDate, Type: datetime  
Name: VariableChargeEndDate, Type: datetime  
Name: UnitNumber, Type: varchar(20)  
Name: VIN, Type: varchar(20)  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: Year, Type: int  
Name: PreviouslyBilledMeter, Type: decimal  
Name: MeterAtBilling, Type: decimal  
Name: UnitFixedChargeTotal, Type: decimal  
Name: UnitVariableChargeTotal, Type: decimal  
Name: UnitMiscChargeTotal, Type: decimal  
Name: UnitTotal, Type: decimal  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: ContractSalesperson, Type: varchar(50)  
Name: UnitSalesperson, Type: varchar(20)  
Name: TotalTax, Type: decimal  
Name: InvoiceTotal, Type: decimal  
Name: UnitPO, Type: varchar(50)  
Name: UnitFixedChargesPO, Type: varchar(50)  
Name: UnitVariableChargesPO, Type: varchar(50)  
Name: UnitMiscChargesPO, Type: varchar(50)


---



### LRCharges

Key: LRCharges,  
Type: View,  
Command: vwLR_SSR_LRCharges,  
HasReturn: false,  
ReturnType:  
DefaultSort: Charge,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseRentalChargeID, Type: int  
Name: Charge, Type: varchar(15)  
Name: InvoiceDescription, Type: varchar(50)  
Name: Lease, Type: bit  
Name: Maintenance, Type: bit  
Name: Rental, Type: bit  
Name: ChargeType, Type: varchar(50)  
Name: BillingFrequency, Type: varchar(50)  
Name: DescOverride, Type: bit  
Name: CostRequired, Type: bit  
Name: Inactive, Type: bit  
Name: TaxStatusOverride, Type: varchar(50)  
Name: TaxCode, Type: varchar(50)  
Name: ProductClass, Type: varchar(50)  
Name: UpdateUser, Type: varchar(20)  
Name: AddUser, Type: varchar(20)  
Name: MeterType, Type: varchar(50)  
Name: LeaseRentalChargeType, Type: varchar(50)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime


---



### LRContract 

Key: LRContract,  
Type: View,  
Command: vwLR_SSR_LRContract,  
HasReturn: false,  
ReturnType:  
DefaultSort: ContractNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseContractID, Type: int  
Name: FixedCharegesBillingID, Type: int  
Name: VariableCharegesBillingID, Type: int  
Name: ContractNumber, Type: int  
Name: LeaseContractStatus, Type: varchar(50)  
Name: BranchID, Type: int  
Name: BranchCode, Type: varchar(10)  
Name: DepartmentID, Type: int  
Name: Department, Type: varchar(10)  
Name: UserName, Type: varchar(20)  
Name: CustomerID, Type: int  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: StartDate, Type: datetime  
Name: AddressType, Type: varchar(50)  
Name: DOT, Type: varchar(100)  
Name: CVOR, Type: varchar(100)  
Name: FixedChargeBillingGroup, Type: varchar(50)  
Name: VariableChargeBillingGroup, Type: varchar(50)  
Name: CustomerPO, Type: varchar(50)  
Name: TaxStatus, Type: varchar(50)  
Name: TaxBody, Type: varchar(50)  
Name: UserDefinedPaymentMethod, Type: varchar(50)  
Name: Address1, Type: varchar(100)  
Name: Address2, Type: varchar(100)  
Name: City, Type: varchar(100)  
Name: Region, Type: varchar(6)  
Name: PostalCode, Type: varchar(15)  
Name: Country, Type: varchar(100)  
Name: County, Type: varchar(100)  
Name: Phone, Type: varchar(30)  
Name: Phone2, Type: varchar(30)  
Name: Phone3, Type: varchar(30)  
Name: Fax, Type: varchar(30)  
Name: EMail, Type: varchar(100)  
Name: WebAddress, Type: varchar(100)  
Name: ContractType, Type: varchar(20)  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: SalesTaxSetting, Type: varchar(8)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime  
Name: SubsAllowed, Type: bit  
Name: FixedChargesPO, Type: varchar(50)  
Name: VariableChargesPO, Type: varchar(50)  
Name: MiscChargesPO, Type: varchar(50)


---



### LRContractUnit 

Key: LRContractUnit,  
Type: View,  
Command: vwLR_SSR_LRContractUnit,  
HasReturn: false,  
ReturnType:  
DefaultSort: ContractNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseContractID, Type: int  
Name: CustomerInsuranceID, Type: int  
Name: CustomerID, Type: int  
Name: UnitInventoryID, Type: int  
Name: RentalRateID, Type: int  
Name: LeaseContractUnitID, Type: int  
Name: BranchID, Type: int  
Name: DriverLicenseID, Type: int  
Name: LeaseContractStatus, Type: varchar(50)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: CharacteristicType, Type: varchar(20)  
Name: LastBillThruFixed, Type: datetime  
Name: LastBillThruVariable, Type: datetime  
Name: ContractNumber, Type: int  
Name: LeaseContractUnitStatus, Type: varchar(50)  
Name: UserName, Type: varchar(20)  
Name: CustomerPO, Type: varchar(50)  
Name: ReturnBranch, Type: varchar(10)  
Name: UnitNumber, Type: varchar(20)  
Name: RentalRate, Type: varchar(15)  
Name: UnitIndicator, Type: varchar(50)  
Name: ProductionYear, Type: datetime  
Name: MeterReading, Type: decimal  
Name: FleetType, Type: varchar(50)  
Name: Make, Type: varchar(50)  
Name: EquipmentType, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: EquipmentClass, Type: varchar(50)  
Name: Vin, Type: varchar(20)  
Name: OutDate, Type: datetime  
Name: ReturnDate, Type: datetime  
Name: Term, Type: int  
Name: IsNoReturnDate, Type: bit  
Name: EstimatedBilledMeter, Type: int  
Name: TotalBilledMeter, Type: int  
Name: StaringCPI, Type: decimal  
Name: LastCPI, Type: decimal  
Name: IsSubjectToCPI, Type: bit  
Name: MonthsBeforeCPICalculated, Type: int  
Name: AllowedForFixed, Type: decimal  
Name: AllowedForVariable, Type: decimal  
Name: MaxAnnualofIncreaseFixed, Type: decimal  
Name: MaxAnnualofIncreaseVariable, Type: decimal  
Name: MaxAnnualMeter, Type: decimal  
Name: MinAnnualMeter, Type: decimal  
Name: PreviouslyBilledMeter, Type: decimal  
Name: Commodity, Type: varchar(50)  
Name: IsHazardous, Type: bit  
Name: Area, Type: varchar(50)  
Name: StartingMeter, Type: decimal  
Name: EndingMeter, Type: decimal  
Name: MeterAllowance, Type: decimal  
Name: InsuranceProvider, Type: varchar(100)  
Name: PolicyNumber, Type: varchar(100)  
Name: ExpirationDate, Type: datetime  
Name: LicenseNumber, Type: varchar(50)  
Name: FirstName, Type: varchar(100)  
Name: DriverMiddleInitial, Type: char  
Name: LastName, Type: varchar(100)  
Name: LicenseExpiration, Type: datetime  
Name: BillFuelTicketOnLRInvoice, Type: bit  
Name: ParentUnitNumber, Type: varchar(20)  
Name: ChildUnits, Type: bit  
Name: ChildUnitsOnContract, Type: bit  
Name: SubsAllowed, Type: bit  
Name: OriginalUnit, Type: varchar(20)  
Name: SubUnit, Type: bit  
Name: PhysicalDamageInsuranceProvider, Type: varchar(100)  
Name: PhysicalDamageInsurancePolicyNumber, Type: varchar(100)  
Name: PhysicalDamangeInsuranceExpirationDate, Type: datetime  
Name: PhysicalDamangeInsuranceID, Type: int  
Name: UnitFixedChargesPO, Type: varchar(50)  
Name: UnitVariableChargesPO, Type: varchar(50)  
Name: UnitMiscChargesPO, Type: varchar(50)  
Name: BillingReserve, Type: decimal


---



### LRContractUnitCharge 

Key: LRContractUnitCharge,  
Type: View,  
Command: vwLR_SSR_LRContractUnitCharge,  
HasReturn: false,  
ReturnType:  
DefaultSort: ContractNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseContractChargeID, Type: int  
Name: LeaseContractID, Type: int  
Name: ContractNumber, Type: int  
Name: LeaseContractUnitID, Type: int  
Name: UnitInventoryID, Type: int  
Name: UnitNumber, Type: varchar(20)  
Name: LeaseRentalChargeID, Type: int  
Name: Charge, Type: varchar(15)  
Name: Description, Type: varchar(100)  
Name: BillingRateFrequency, Type: varchar(50)  
Name: MeterType, Type: varchar(50)  
Name: Cost, Type: decimal  
Name: Rate, Type: decimal  
Name: LeaseRentalChargeType, Type: varchar(50)  
Name: OverrideDescription, Type: varchar(100)  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime


---



### LRCustomerRateOverrideDetail 

Key: LRCustomerRateOverrideDetail,  
Type: View,  
Command: vwLR_SSR_LRCustomerRateOverrideDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: Customer,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseRentalCustomerRateOverrideID, Type: int  
Name: RentalRateID, Type: int  
Name: BranchID, Type: int  
Name: CustomerID, Type: int  
Name: RentalRateLeaseRentalChargeID, Type: int  
Name: LeaseRentalChargeID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Customer, Type: varchar(10)  
Name: CustomerName, Type: varchar(100)  
Name: LRRate, Type: varchar(15)  
Name: LRRateDescription, Type: varchar(50)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateUser, Type: varchar(20)  
Name: Charge, Type: varchar(15)  
Name: ChargeDescription, Type: varchar(50)  
Name: ChargeType, Type: varchar(50)  
Name: BillingFrequency, Type: varchar(50)  
Name: MeterType, Type: varchar(50)  
Name: Cost, Type: decimal  
Name: Rate, Type: decimal  
Name: OverrideRate, Type: decimal  
Name: Multiplier, Type: decimal  
Name: OverrideMethod, Type: varchar(10)


---



### LRCustomerRateOverrideHeader 

Key: LRCustomerRateOverrideHeader,  
Type: View,  
Command: vwLR_SSR_LRCustomerRateOverrideHeader,  
HasReturn: false,  
ReturnType:  
DefaultSort: Customer,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LeaseRentalCustomerRateOverrideID, Type: int  
Name: RentalRateID, Type: int  
Name: BranchID, Type: int  
Name: CustomerID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Customer, Type: varchar(10)  
Name: CustomerName, Type: varchar(100)  
Name: LRRate, Type: varchar(15)  
Name: LRRateDescription, Type: varchar(50)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateUser, Type: varchar(20)


---



### LRUnits 

Key: LRUnits,  
Type: View,  
Command: vwLR_SSR_LRUnits,  
HasReturn: false,  
ReturnType:  
DefaultSort: UnitNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: UnitInventoryID, Type: int  
Name: ProductionYear, Type: datetime  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: Manufacturer, Type: varchar(50)  
Name: Vin, Type: varchar(20)  
Name: SerialNumber, Type: varchar(20)  
Name: UnitIndicator, Type: varchar(50)  
Name: CharacteristicType, Type: varchar(20)  
Name: UnitNumber, Type: varchar(20)  
Name: FleetNumber, Type: varchar(10)  
Name: FleetType, Type: varchar(50)  
Name: EquipmentType, Type: varchar(50)  
Name: EquipmentClass, Type: varchar(50)  
Name: LRUnitStatus, Type: varchar(50)  
Name: BranchID, Type: int  
Name: OwningBranchCode, Type: varchar(10)  
Name: LocationBranchCode, Type: varchar(10)  
Name: CustomerID, Type: int  
Name: CustomerKey, Type: varchar(10)  
Name: RentalRate, Type: varchar(15)  
Name: MeterReading, Type: decimal  
Name: MeterType, Type: varchar(50)  
Name: PrimaryLicenseNumber, Type: varchar(50)  
Name: IsSaleUnit, Type: bit  
Name: LotLocation, Type: varchar(20)  
Name: LotLocationBranch, Type: varchar(10)  
Name: BillingMeterReading, Type: decimal  
Name: BillingMeterReadingDate, Type: datetime  
Name: FirstTaxableUse, Type: datetime  
Name: RegisteredWeight, Type: int  
Name: RegisteredWeightCategory, Type: varchar(1)  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: CurrentLRContractBranch, Type: varchar(10)  
Name: CurrentLRContract, Type: int  
Name: CurrentLRContractCustomer, Type: varchar(100)  
Name: CurrentLRContractOutDate, Type: datetime  
Name: CurrentLRContractReturnDate, Type: datetime  
Name: GVWR, Type: int  
Name: FinanceSource, Type: varchar(50)  
Name: LRUnitMessage, Type: varchar(7500)  
Name: IsRepairOrderComment, Type: bit  
Name: LRUnitMessageAddUser, Type: varchar(20)  
Name: LRUnitMessageDate, Type: date


---



### PermitandLicense 

Key: PermitandLicense,  
Type: View,  
Command: vwLR_SSR_PermitandLicense,  
HasReturn: false,  
ReturnType:  
DefaultSort: UnitNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PermitLicenseID, Type: int  
Name: UnitInventoryID, Type: int  
Name: PermitLicenseNumber, Type: varchar(50)  
Name: PermitType, Type: varchar(15)  
Name: UnitNumber, Type: varchar(20)  
Name: Region, Type: varchar(6)  
Name: RegionName, Type: varchar(50)  
Name: ExpirationDate, Type: datetime  
Name: Fee, Type: money  
Name: Inactive, Type: bit  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime

## Sales



---



### LPO 

Key: LPO,  
Type: View,  
Command: vwSM_SSR_LPO,  
HasReturn: false,  
ReturnType:  
DefaultSort: LPO,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: CustomerID, Type: int  
Name: RepairOrderID, Type: int  
Name: UnitInventoryID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: LPO, Type: int  
Name: Status, Type: varchar(50)  
Name: OrderedBy, Type: varchar(20)  
Name: IssueDate, Type: datetime  
Name: ControlBranch, Type: varchar(10)  
Name: ControlDepartment, Type: varchar(10)  
Name: UnitIndicator, Type: varchar(50)  
Name: CharacteristicType, Type: varchar(20)  
Name: InventoryType, Type: varchar(20)  
Name: StockNumber, Type: varchar(20)  
Name: UnitNumber, Type: varchar(20)  
Name: SerialNumber, Type: varchar(20)  
Name: Year, Type: int  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: VIN, Type: varchar(20)  
Name: LPOType, Type: varchar(20)  
Name: Usage, Type: varchar(50)  
Name: Description, Type: varchar(50)  
Name: Addon, Type: varchar(20)  
Name: AddOnName, Type: varchar(50)  
Name: AddOnPrice, Type: decimal  
Name: ToVendorNumber, Type: varchar(20)  
Name: ToVendor, Type: varchar(100)  
Name: ToBranch, Type: varchar(10)  
Name: ToDepartment, Type: varchar(10)  
Name: ExpectedAmount, Type: decimal  
Name: IsLimit, Type: bit  
Name: ExpectedCloseDate, Type: datetime  
Name: CurrencyCode, Type: varchar(10)  
Name: LPOCostConversion, Type: varchar(50)  
Name: CloseDate, Type: datetime  
Name: ActualAmount, Type: decimal  
Name: OverUnder, Type: decimal  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: InvoiceNumber, Type: varchar(50)  
Name: DealNumber, Type: int  
Name: RONumber, Type: int  
Name: ShipToAddress1, Type: varchar(100)  
Name: ShipToAddress2, Type: varchar(100)  
Name: ShipToCity, Type: varchar(100)  
Name: ShipToRegion, Type: varchar(6)  
Name: ShipToPostalCode, Type: varchar(15)  
Name: ShipToCountry, Type: varchar(35)  
Name: ShipToCounty, Type: varchar(35)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime


---



### SalesDealCommission 

Key: SalesDealCommission,  
Type: View,  
Command: vwSM_SSR_SalesDealCommission,  
HasReturn: false,  
ReturnType:  
DefaultSort: DealNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: DealCommissionInvoiceID, Type: int  
Name: DealPacketInvoiceID, Type: int  
Name: DealUnitInvoiceID, Type: int  
Name: UnitInventoryID, Type: int  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: DealNumber, Type: varchar(20)  
Name: PacketNumber, Type: varchar(20)  
Name: Salesperson, Type: varchar(224)  
Name: SoldStockNumber, Type: varchar(20)  
Name: Year, Type: int  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: InventoryType, Type: varchar(20)  
Name: InvoiceDate, Type: datetime  
Name: BaseCost, Type: money  
Name: OpenLPOs, Type: decimal  
Name: Price, Type: decimal  
Name: Cost, Type: money  
Name: Profit, Type: decimal  
Name: TotalAddonPrice, Type: money  
Name: TotalAddonCost, Type: money  
Name: TotalAddonProfit, Type: money  
Name: ProratedOverUnderAllowance, Type: money  
Name: Misc1, Type: varchar(50)  
Name: Misc1Price, Type: decimal  
Name: Misc1Cost, Type: decimal  
Name: Misc1Profit, Type: decimal  
Name: Misc2, Type: varchar(50)  
Name: Misc2Price, Type: decimal  
Name: Misc2Cost, Type: decimal  
Name: Misc2Profit, Type: decimal  
Name: IncludeFinanceReserveInTotalProfit, Type: bit  
Name: IncludeInsuranceIncomeInTotalProfit, Type: bit  
Name: FinanceLender, Type: varchar(100)  
Name: FinanceReserve, Type: money  
Name: FinanceCommission, Type: money  
Name: InsuranceIncome, Type: money  
Name: InsuranceCommission, Type: money  
Name: MinimumProfit, Type: money  
Name: MinimumProfitPercentage, Type: decimal  
Name: CommissionPercentage, Type: decimal  
Name: FlatAmount, Type: money  
Name: MinimumCommission, Type: money  
Name: IsCommissionPercentageAgainstProfit, Type: bit  
Name: TotalPrice, Type: decimal  
Name: TotalCost, Type: decimal  
Name: TotalProfit, Type: decimal  
Name: Commission, Type: decimal  
Name: CommissionDate, Type: datetime  
Name: Held, Type: bit  
Name: HeldDate, Type: datetime  
Name: HeldReason, Type: varchar(50)  
Name: Approved, Type: bit  
Name: Note, Type: varchar(50)


---



### SalesDealDetail 

Key: SalesDealDetail,  
Type: View,  
Command: vwSM_SSR_SalesDealDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: DealHeaderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: DealHeaderID, Type: int  
Name: DealPacketID, Type: int  
Name: DealPacketInvoiceID, Type: int  
Name: BranchID, Type: int  
Name: UnitInventoryID, Type: int  
Name: DetailID, Type: int  
Name: SortOrder, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: DealHeaderNumber, Type: int  
Name: DealPacketNumber, Type: smallint  
Name: OrderStatus, Type: varchar(50)  
Name: InvoiceNumber, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: StockNumber, Type: varchar(20)  
Name: ItemType, Type: varchar(50)  
Name: Item, Type: varchar(100)  
Name: ItemDescription, Type: varchar(110)  
Name: Price, Type: decimal  
Name: Cost, Type: money  
Name: Profit, Type: decimal  
Name: ProfitMargin, Type: decimal  
Name: ProfitCalculation, Type: varchar(50)  
Name: SaleType, Type: varchar(20)  
Name: InventoryType, Type: varchar(20)  
Name: TradeInActualCashValue, Type: money  
Name: TradeInAllowance, Type: decimal  
Name: TradeInOverUnderAllowance, Type: decimal  
Name: Rate, Type: decimal  
Name: BuyRate, Type: decimal  
Name: FinanceReserve, Type: decimal  
Name: Period, Type: smallint  
Name: PrePosted, Type: bit  
Name: Refunded, Type: bit  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: TireTaxCredit, Type: decimal  
Name: FETAmount, Type: decimal  
Name: ExemptEquipment, Type: decimal  
Name: ExemptDelivery, Type: decimal  
Name: AmountSubjectToFET, Type: decimal


---



### SalesDealHeader 

Key: SalesDealHeader,  
Type: View,  
Command: vwSM_SSR_SalesDealHeader,  
HasReturn: false,  
ReturnType:  
DefaultSort: DealNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: DealHeaderID, Type: int  
Name: BranchID, Type: int  
Name: CustomerID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: DealNumber, Type: int  
Name: IsWorksheet, Type: bit  
Name: Salesperson, Type: varchar(20)  
Name: SalespersonName, Type: varchar(201)  
Name: SaleType, Type: varchar(20)  
Name: PaymentMethod, Type: varchar(50)  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: CustomerPO, Type: varchar(20)  
Name: DealStatus, Type: varchar(50)  
Name: TaxStatus, Type: varchar(50)  
Name: TaxBasis, Type: varchar(8)  
Name: TaxBody, Type: varchar(50)  
Name: TaxRegion, Type: varchar(6)  
Name: TotalUnitPrice, Type: decimal  
Name: TotalUnitCost, Type: money  
Name: TotalUnitAddOnPrice, Type: decimal  
Name: TotalUnitAddOnCost, Type: money  
Name: TotalTradeInAllowance, Type: decimal  
Name: TotalTradeInActualCashValue, Type: money  
Name: TotalDealAddOnPrice, Type: decimal  
Name: TotalDealAddOnCost, Type: money  
Name: TotalFET, Type: decimal  
Name: TotalSalesTax, Type: decimal  
Name: TotalPayoffs, Type: decimal  
Name: TotalDeposits, Type: decimal  
Name: TotalDownPayments, Type: decimal  
Name: TotalFinanced, Type: decimal  
Name: TotalFinanceReserve, Type: decimal  
Name: TotalUnitFinanced, Type: decimal  
Name: TotalUnitFinanceReserve, Type: decimal  
Name: TotalProfitUnitAddOnPrice, Type: decimal  
Name: TotalProfitUnitAddOnCost, Type: money  
Name: TotalNonProfitUnitAddOnPrice, Type: decimal  
Name: TotalNonProfitUnitAddOnCost, Type: money  
Name: TotalProfitDealAddOnPrice, Type: decimal  
Name: TotalProfitDealAddOnCost, Type: money  
Name: TotalNonProfitDealAddOnPrice, Type: decimal  
Name: TotalNonProfitDealAddOnCost, Type: money  
Name: TotalProfit, Type: decimal  
Name: TotalProfitPercent, Type: decimal  
Name: Commission, Type: decimal  
Name: QuoteDate, Type: datetime  
Name: ExpirationDate, Type: datetime  
Name: PaidDate, Type: datetime  
Name: DeliveryDate, Type: datetime  
Name: SignDate, Type: datetime  
Name: IsFinancingRequired, Type: bit  
Name: IsFinancingApproved, Type: bit  
Name: IsCustomerPickup, Type: bit  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)


---



### SalesDealPacket 

Key: SalesDealPacket,  
Type: View,  
Command: vwSM_SSR_SalesDealPacket,  
HasReturn: false,  
ReturnType:  
DefaultSort: DealNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: DealHeaderID, Type: int  
Name: DealPacketID, Type: int  
Name: DealPacketInvoiceID, Type: int  
Name: BranchID, Type: int  
Name: CustomerID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: DealNumber, Type: int  
Name: PacketNumber, Type: smallint  
Name: DealPacketStatus, Type: varchar(50)  
Name: DealContractDate, Type: datetime  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: CustomerPO, Type: varchar(20)  
Name: Salesperson, Type: varchar(20)  
Name: PaymentMethod, Type: varchar(50)  
Name: SalesType, Type: varchar(20)  
Name: TotalUnitPrice, Type: decimal  
Name: TotalUnitCost, Type: money  
Name: TotalUnitAddOnPrice, Type: decimal  
Name: TotalUnitAddOnCost, Type: money  
Name: TotalTradeInAllowance, Type: decimal  
Name: TotalActualCashValue, Type: money  
Name: TotalDealAddOnPrice, Type: decimal  
Name: TotalDealAddOnCost, Type: money  
Name: TotalFET, Type: decimal  
Name: TotalSalesTax, Type: decimal  
Name: TotalPayoff, Type: decimal  
Name: TotalDeposits, Type: decimal  
Name: TotalDownPayments, Type: decimal  
Name: TotalFinanced, Type: decimal  
Name: TotalFinanceReserve, Type: decimal  
Name: FinanceAmount, Type: decimal  
Name: FinanceReserve, Type: decimal  
Name: TotalProfitUnitAddOnPrice, Type: decimal  
Name: TotalProfitUnitAddOnCost, Type: money  
Name: TotalNonProfitUnitAddOnPrice, Type: decimal  
Name: TotalNonProfitUnitAddOnCost, Type: money  
Name: TotalProfitDealAddOnPrice, Type: decimal  
Name: TotalProfitDealAddOnCost, Type: money  
Name: TotalNonProfitDealAddOnPrice, Type: decimal  
Name: TotalNonProfitDealAddOnCost, Type: money  
Name: TotalProfitPercent, Type: decimal  
Name: TotalProfit, Type: decimal  
Name: SignDate, Type: datetime  
Name: DeliveryDate, Type: datetime  
Name: InvoiceDate, Type: datetime  
Name: InvoiceNumber, Type: varchar(20)  
Name: JournalBranch, Type: varchar(10)  
Name: JournalReference, Type: varchar(30)  
Name: CurrencyCode, Type: varchar(10)  
Name: OverrideExchangeRate, Type: decimal  
Name: PostDate, Type: datetime  
Name: PostPeriod, Type: varchar(7)  
Name: Journal, Type: varchar(10)  
Name: CommissionPostDate, Type: datetime  
Name: CommissionPostMonth, Type: varchar(7)  
Name: CommissionPostJournal, Type: int  
Name: InvoiceName1, Type: varchar(100)  
Name: InvoiceName2, Type: varchar(100)  
Name: ContactAddress1, Type: varchar(100)  
Name: ContactAddress2, Type: varchar(100)  
Name: ContactTaxBody, Type: varchar(50)  
Name: ContactCity, Type: varchar(100)  
Name: ContactRegion, Type: varchar(6)  
Name: ContactPostalCode, Type: varchar(15)  
Name: ContactCountry, Type: varchar(35)  
Name: ContactCounty, Type: varchar(35)  
Name: BillToAddress1, Type: varchar(100)  
Name: BillToAddress2, Type: varchar(100)  
Name: BillToTaxBody, Type: varchar(50)  
Name: BillToCity, Type: varchar(100)  
Name: BillToRegion, Type: varchar(6)  
Name: BillToPostalCode, Type: varchar(15)  
Name: BillToCountry, Type: varchar(35)  
Name: BillToCounty, Type: varchar(35)  
Name: ShipToAddress1, Type: varchar(100)  
Name: ShipToAddress2, Type: varchar(100)  
Name: ShipToTaxBody, Type: varchar(50)  
Name: ShipToCity, Type: varchar(100)  
Name: ShipToRegion, Type: varchar(6)  
Name: ShipToPostalCode, Type: varchar(15)  
Name: ShipToCountry, Type: varchar(35)  
Name: ShipToCounty, Type: varchar(35)  
Name: TaxBasis, Type: varchar(8)  
Name: TaxStatus, Type: varchar(50)  
Name: TaxBody, Type: varchar(50)  
Name: TaxRegion, Type: varchar(6)  
Name: Commission, Type: decimal  
Name: PostedAfterSalesCommission, Type: decimal  
Name: PostedAfterSalesExpense, Type: money  
Name: FinanceCommission, Type: money  
Name: InsuranceIncome, Type: money  
Name: InsuranceCommission, Type: money  
Name: AddUser, Type: varchar(20)  
Name: InvoiceUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: JournalCode, Type: int  
Name: TransactionType, Type: int


---



### SalesUnit 

Key: SalesUnit,  
Type: View,  
Command: vwSM_SSR_SalesUnit,  
HasReturn: false,  
ReturnType:  
DefaultSort: SoldInvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: UnitID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: UnitInventoryID, Type: int  
Name: Max View Date, Type: datetime  
Name: LPO Actual Cost, Type: decimal  
Name: Year, Type: char  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: Manufacturer, Type: varchar(50)  
Name: VIN, Type: varchar(20)  
Name: SerialNumber, Type: varchar(20)  
Name: UnitIndicator, Type: varchar(50)  
Name: Barcode, Type: varchar(40)  
Name: CharacteristicType, Type: varchar(20)  
Name: Inactive, Type: bit  
Name: IsActiveUnit, Type: bit  
Name: UsageType, Type: varchar(20)  
Name: GVWR, Type: int  
Name: MeterType, Type: varchar(50)  
Name: CurrentMeterReading, Type: decimal  
Name: CurrentMeterReadingDate, Type: datetime  
Name: CurrentECMReading, Type: decimal  
Name: CurrentECMReadingDate, Type: datetime  
Name: LotLocation, Type: varchar(20)  
Name: TemporaryLocationType, Type: varchar(50)  
Name: TemporaryLocationName, Type: varchar(111)  
Name: AcquisitionMethod, Type: varchar(50)  
Name: Consignor, Type: varchar(10)  
Name: IsLeaseRentalUnit, Type: bit  
Name: AcquisitionDate, Type: datetime  
Name: AcquiringSalesperson, Type: varchar(20)  
Name: PONumber, Type: int  
Name: FactoryOrderNumber, Type: varchar(20)  
Name: PurchaseOrderStatus, Type: varchar(50)  
Name: PurchaseUnitStatus, Type: varchar(50)  
Name: OrderDate, Type: datetime  
Name: VoidOrderDate, Type: datetime  
Name: BuildDate, Type: datetime  
Name: RequestShipDate, Type: datetime  
Name: ActualShipDate, Type: datetime  
Name: EstimatedArrivalDate, Type: datetime  
Name: ReceiveInvoiceDate, Type: datetime  
Name: InvoicePostedDate, Type: datetime  
Name: ReceiveInvoiceNumber, Type: varchar(20)  
Name: JournalSequence, Type: int  
Name: ReceivedDate, Type: datetime  
Name: DaysInInventory-ReceiveDate, Type: int  
Name: DaysInInventory-ReceiveInvoiceDate, Type: int  
Name: DaysInInventory, Type: int  
Name: PreviousOwner, Type: varchar(50)  
Name: ReplenishStock, Type: bit  
Name: CurrentTitleNumber, Type: varchar(30)  
Name: TitleRegion, Type: varchar(6)  
Name: FlooringBalance, Type: decimal  
Name: AvailabilityStatus, Type: varchar(50)  
Name: SellingStatus, Type: varchar(50)  
Name: ControlBranch, Type: varchar(10)  
Name: BookBranch, Type: varchar(10)  
Name: ControlDepartment, Type: varchar(10)  
Name: InventoryType, Type: varchar(50)  
Name: StockNumber, Type: varchar(20)  
Name: BaseCost, Type: money  
Name: CurrentCost, Type: decimal  
Name: OpenLpos, Type: decimal  
Name: TotalUnitCost, Type: decimal  
Name: PurchaseCost, Type: money  
Name: NewUnit, Type: bit  
Name: Export, Type: bit  
Name: TradeInAllowance, Type: decimal  
Name: ActualCashValue, Type: decimal  
Name: CurrencyCode, Type: varchar(10)  
Name: UnitCostConversion, Type: varchar(50)  
Name: UnitCostConverted, Type: bit  
Name: ListPrice, Type: decimal  
Name: AskingPrice, Type: decimal  
Name: LowPrice, Type: decimal  
Name: SpecialPrice, Type: decimal  
Name: SpecialPriceExpiration, Type: varchar(30)  
Name: ProductClass, Type: varchar(50)  
Name: FETCharged, Type: bit  
Name: TireTaxCredit, Type: decimal  
Name: FETExemptDeliveryExpenses, Type: decimal  
Name: FETExemptEquipment, Type: decimal  
Name: SoldCustomerKey, Type: varchar(10)  
Name: SoldCustomerName, Type: varchar(100)  
Name: SoldCustomerAddress1, Type: varchar(100)  
Name: SoldCustomerAddress2, Type: varchar(100)  
Name: SoldCustomerCity, Type: varchar(100)  
Name: SoldCustomerRegion, Type: varchar(6)  
Name: SoldCustomerPostalCode, Type: varchar(15)  
Name: SoldCustomerCountry, Type: varchar(50)  
Name: SoldCustomerCounty, Type: varchar(50)  
Name: SoldDate, Type: datetime  
Name: SoldInvoiceNumber, Type: varchar(20)  
Name: SoldPrice, Type: decimal  
Name: SoldCost, Type: money  
Name: Holdback, Type: decimal  
Name: SoldSalesperson, Type: varchar(20)  
Name: InServiceDealerCode, Type: varchar(20)  
Name: InServiceDate, Type: datetime  
Name: InServiceMeterReading, Type: decimal  
Name: WarrantyMeter, Type: decimal  
Name: PeriodType, Type: varchar(50)  
Name: WarrantyPeriod, Type: int  
Name: WarrantyContract, Type: varchar(50)


---



### UnitFlooring 

Key: UnitFlooring,  
Type: View,  
Command: vwSM_SSR_UnitFlooring,  
HasReturn: false,  
ReturnType:  
DefaultSort: SerialNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: UnitFlooringInfoID, Type: int  
Name: UnitInventoryID, Type: int  
Name: StockNumber, Type: varchar(20)  
Name: InventoryType, Type: varchar(20)  
Name: Year, Type: int  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: Manufacturer, Type: varchar(50)  
Name: Vin, Type: varchar(20)  
Name: SerialNumber, Type: varchar(20)  
Name: BarCode, Type: varchar(40)  
Name: CharacteristicType, Type: varchar(50)  
Name: Inactive, Type: bit  
Name: AvailabilityStatus, Type: varchar(50)  
Name: SellingStatus, Type: varchar(50)  
Name: ControlBranch, Type: varchar(10)  
Name: ControlDepartment, Type: varchar(10)  
Name: BookBranch, Type: varchar(10)  
Name: SoldDate, Type: datetime  
Name: FloorPlanLender, Type: varchar(100)  
Name: FloorPlanLenderDescription, Type: varchar(100)  
Name: Plan, Type: varchar(50)  
Name: AgreementNumber, Type: varchar(20)  
Name: PackRate, Type: decimal  
Name: FlooringAmount, Type: decimal  
Name: FlooringBalance, Type: decimal  
Name: FlooringStartDate, Type: datetime  
Name: ExpensesToDate, Type: decimal  
Name: LastPostDate, Type: datetime  
Name: PayoffDate, Type: datetime  
Name: DaysFloored, Type: int  
Name: AU, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime


---



### UnitPurchaseOrderDetail

Key: UnitPurchaseOrderDetail,  
Type: View,  
Command: vwSM_SSR_UnitPurchaseOrderDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: PONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: PurchaseOrderID, Type: int  
Name: UnitInventoryID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: PONumber, Type: int  
Name: Supplier, Type: varchar(10)  
Name: SupplierName, Type: varchar(100)  
Name: PODate, Type: datetime  
Name: PurchasingStatus, Type: varchar(50)  
Name: OrderDate, Type: datetime  
Name: ClosedDate, Type: datetime  
Name: DealNumber, Type: int  
Name: Customer, Type: varchar(10)  
Name: CustomerPO, Type: varchar(20)  
Name: Salesperson, Type: varchar(20)  
Name: StockNumber, Type: varchar(20)  
Name: VIN, Type: varchar(20)  
Name: SerialNumber, Type: varchar(20)  
Name: InventoryType, Type: varchar(20)  
Name: Year, Type: int  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: AcquisitionMethod, Type: varchar(50)  
Name: AcquisitionDate, Type: datetime  
Name: AcquiringSalesperson, Type: varchar(201)  
Name: BuildDate, Type: datetime  
Name: RequestedShipDate, Type: datetime  
Name: ActualShipDate, Type: datetime  
Name: EstimatedArrivalDate, Type: datetime  
Name: CurrencyCode, Type: varchar(10)  
Name: BaseCost, Type: money  
Name: UnitShipToAddressStreet1, Type: varchar(100)  
Name: UnitShipToAddressStreet2, Type: varchar(100)  
Name: UnitShipToAddressCity, Type: varchar(100)  
Name: UnitShipToAddressRegion, Type: varchar(6)  
Name: UnitShipToAddressPostalCode, Type: varchar(15)  
Name: UnitShipToAddressCountry, Type: varchar(35)  
Name: UnitShipToAddressCounty, Type: varchar(35)  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)


---



### UnitPurchaseOrderHeader 

Key: UnitPurchaseOrderHeader,  
Type: View,  
Command: vwSM_SSR_UnitPurchaseOrderHeader,  
HasReturn: false,  
ReturnType:  
DefaultSort: PONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: PurchaseOrderID, Type: int  
Name: CustomerID, Type: int  
Name: ShipToAddressID, Type: int  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: PONumber, Type: int  
Name: POType, Type: varchar(50)  
Name: PurchasingStatus, Type: varchar(50)  
Name: PODate, Type: datetime  
Name: ClosedDate, Type: datetime  
Name: SupplierType, Type: varchar(8)  
Name: Supplier, Type: varchar(10)  
Name: SupplierName, Type: varchar(100)  
Name: FactoryOrderNumber, Type: varchar(20)  
Name: WorkPhone, Type: varchar(30)  
Name: Fax, Type: varchar(30)  
Name: HomePhone, Type: varchar(30)  
Name: Pager, Type: varchar(30)  
Name: CellPhone, Type: varchar(30)  
Name: EmailAddress, Type: varchar(100)  
Name: WebAddress, Type: varchar(100)  
Name: ShipToAddressStreet1, Type: varchar(100)  
Name: ShipToAddressStreet2, Type: varchar(100)  
Name: ShipToAddressCity, Type: varchar(100)  
Name: ShipToAddressRegion, Type: varchar(6)  
Name: ShipToAddressPostalCode, Type: varchar(15)  
Name: ShipToAddressCountry, Type: varchar(35)  
Name: ShipToAddressCounty, Type: varchar(35)  
Name: SupplierBillToAddressStreet1, Type: varchar(100)  
Name: SupplierBillToAddressStreet2, Type: varchar(100)  
Name: SupplierBillToAddressCity, Type: varchar(100)  
Name: SupplierBillToAddressRegion, Type: varchar(6)  
Name: SupplierBillToAddressPostalCode, Type: varchar(15)  
Name: SupplierBillToAddressCountry, Type: varchar(35)  
Name: SupplierBillToAddressCounty, Type: varchar(35)  
Name: BranchBillToAddressStreet1, Type: varchar(100)  
Name: BranchBillToAddressStreet2, Type: varchar(100)  
Name: BranchBillToAddressCity, Type: varchar(100)  
Name: BranchBillToAddressRegion, Type: varchar(6)  
Name: BranchBillToAddressPostalCode, Type: varchar(15)  
Name: BranchBillToAddressCountry, Type: varchar(35)  
Name: BranchBillToAddressCounty, Type: varchar(35)  
Name: UnitsOutstanding, Type: int  
Name: UnitsReceived, Type: int  
Name: TotalUnitsOrdered, Type: int  
Name: POTotal, Type: money  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)

## Service



---   ### DeferredRepairs 

Key: DeferredRepairs,  
Type: View,  
Command: vwSR_SSR_DeferredRepairs,  
HasReturn: false,  
ReturnType:  
DefaultSort: CustomerNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: DeferringBranch, Type: varchar(10)  
Name: DeferringDepartment, Type: varchar(10)  
Name: CustomerNumber, Type: varchar(10)  
Name: CustomerName, Type: varchar(100)  
Name: Ship-toAddress1, Type: varchar(100)  
Name: Ship-toAddress2, Type: varchar(100)  
Name: Ship-toCity, Type: varchar(100)  
Name: Ship-toRegion, Type: varchar(6)  
Name: Ship-toPostalCode, Type: varchar(15)  
Name: Ship-toCountry, Type: varchar(35)  
Name: Ship-toCounty, Type: varchar(35)  
Name: OfficePhone, Type: varchar(30)  
Name: UnitNumber, Type: varchar(20)  
Name: Vin, Type: varchar(20)  
Name: UnitMake, Type: varchar(50)  
Name: UnitModel, Type: varchar(50)  
Name: UnitYear, Type: datetime  
Name: InServiceDate, Type: datetime  
Name: DeferringRONumber, Type: int  
Name: DeferringTaskNumber, Type: smallint  
Name: RepairGroup, Type: varchar(10)  
Name: RepairGroupDescription, Type: varchar(50)  
Name: RepairType, Type: varchar(12)  
Name: RepairTypeDescription, Type: varchar(50)  
Name: DeferredDate, Type: datetime  
Name: ExpectedExpirationDate, Type: datetime  
Name: DeferredReason, Type: varchar(100)  
Name: DeferringUser, Type: varchar(20)  
Name: RepairTypeID, Type: int  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateUser, Type: varchar(20)


---



### MeterHistory 

Key: MeterHistory,  
Type: View,  
Command: vwSR_SSR_MeterHistory,  
HasReturn: false,  
ReturnType:  
DefaultSort: UnitNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: MeterReadingID, Type: int  
Name: MeterTypeID, Type: int  
Name: MeterType, Type: varchar(50)  
Name: MeterSourceID, Type: int  
Name: MeterSource, Type: varchar(50)  
Name: MeterTransactionTypeID, Type: int  
Name: MeterTransactionType, Type: varchar(50)  
Name: MeterReading, Type: decimal  
Name: MeterDate, Type: datetime  
Name: AverageDailyUsage, Type: int  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: UnitNumber, Type: varchar(20)  
Name: UnitInventoryID, Type: int  
Name: UnitID, Type: int  
Name: Vin, Type: varchar(20)  
Name: CustomerID, Type: int  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: Estimate, Type: bit  
Name: Erroneous, Type: bit  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: ModelYear, Type: int  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime


---



### OpenBarcodeTime 

Key: OpenBarcodeTime,  
Type: View,  
Command: vwSR_SSR_OpenBarcodeTime,  
HasReturn: false,  
ReturnType:  
DefaultSort: TechnicianNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: OpenBarcodeTimeID, Type: int  
Name: RepairOrderID, Type: int  
Name: RepairOrderNumber, Type: int  
Name: RepairOrderTaskID, Type: int  
Name: TaskNumber, Type: smallint  
Name: RepairTypeID, Type: int  
Name: RepairType, Type: varchar(12)  
Name: RepairTypeDescription, Type: varchar(50)  
Name: TechnicianID, Type: int  
Name: TechnicianNumber, Type: int  
Name: TimeIn, Type: datetime  
Name: ShiftID, Type: int  
Name: Shift, Type: varchar(10)  
Name: ShiftDescription, Type: varchar(50)  
Name: BranchID, Type: int  
Name: BranchCode, Type: varchar(10)  
Name: DepartmentID, Type: int  
Name: Department, Type: varchar(10)  
Name: DepartmentDescription, Type: varchar(100)  
Name: IsAvailable, Type: bit  
Name: ElapsedTime, Type: varchar(62)  
Name: ElapsedTime_FH, Type: varchar(30)  
Name: RemainingTime, Type: decimal  
Name: CompletionTime, Type: datetime  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: AddDateTimeZone, Type: decimal  
Name: LastUpdateTimeZone, Type: decimal  
Name: TimeInTimeZone, Type: decimal  
Name: AddApplicationID, Type: int  
Name: AddApplicationNumber, Type: varchar(10)  
Name: UpdateApplicationID, Type: int  
Name: UpdateApplicationNumber, Type: varchar(10)  
Name: TechnicianName, Type: varchar(201)  
Name: ApplicationName, Type: varchar(75)  
Name: UpdateApplicationName, Type: varchar(75)


---



### PreventiveMaintenance 

Key: PreventiveMaintenance,  
Type: View,  
Command: vwSR_SSR_PreventiveMaintenance,  
HasReturn: false,  
ReturnType:  
DefaultSort: UnitNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: CustomerID, Type: int  
Name: AddressID, Type: int  
Name: UnitID, Type: int  
Name: RepairOrderID, Type: int  
Name: RepairOrderTaskID, Type: int  
Name: RepairTypeID, Type: int  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: CustomerBaseBranch, Type: varchar(10)  
Name: ServiceBranch, Type: varchar(10)  
Name: CustomerNumber, Type: varchar(10)  
Name: IsLeaseRentalCustomer, Type: bit  
Name: CompanyName, Type: varchar(100)  
Name: CustomerAddress, Type: varchar(100)  
Name: CustomerCity, Type: varchar(100)  
Name: CustomerRegion, Type: varchar(6)  
Name: CustomerPostalCode, Type: varchar(15)  
Name: CustomerCountry, Type: varchar(35)  
Name: CompanyShopPhone, Type: varchar(30)  
Name: OwningCustomerContact, Type: varchar(201)  
Name: UnitNumber, Type: varchar(20)  
Name: UnitYear, Type: int  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: VIN, Type: varchar(20)  
Name: Ownership, Type: varchar(1)  
Name: PMServiceDue21Days, Type: varchar(1)  
Name: StartingMeter, Type: decimal  
Name: StartingDate, Type: datetime  
Name: AverageDailyUsage, Type: int  
Name: LastMeterDate, Type: datetime  
Name: LastMeterReading, Type: decimal  
Name: UnitType, Type: varchar(20)  
Name: LastRepairOrder, Type: int  
Name: LastInvoiceNumber, Type: varchar(50)  
Name: LastInvoiceDate, Type: datetime  
Name: PMDescription, Type: varchar(50)  
Name: GraceDays, Type: int  
Name: GraceMeter, Type: decimal  
Name: PMBasis, Type: varchar(50)  
Name: PMCode, Type: varchar(20)  
Name: PMMeterInterval, Type: decimal  
Name: PMTimeInterval, Type: int  
Name: PMRepairTypeCode, Type: varchar(12)  
Name: PMRepairTypeDescription, Type: varchar(50)  
Name: PMLastCompletionMeter, Type: decimal  
Name: PMLastCompletionDate, Type: datetime  
Name: PMDateNextDue, Type: datetime  
Name: PMNextMeterDue, Type: decimal  
Name: PMServiceDueFlag, Type: varchar(1)  
Name: PMServiceDue7Days, Type: varchar(1)  
Name: PMServiceDue14Days, Type: varchar(1)  
Name: RONumber, Type: int  
Name: ROStatus, Type: varchar(20)  
Name: RODateOpened, Type: datetime  
Name: TaskNumber, Type: smallint  
Name: TaskDescription, Type: varchar(50)  
Name: TaskClockedOnTechnicians, Type: nvarchar(max)  
Name: IsScheduled, Type: bit  
Name: LastPMROBranch, Type: varchar(10)  
Name: ContractNumber, Type: int  
Name: ContractCompanyName, Type: varchar(100)  
Name: ContractCustomerShopPhone, Type: varchar(30)  
Name: BranchID, Type: int  
Name: OpenPMROBranch, Type: varchar(10)  
Name: ContractCustomerContact, Type: varchar(201)  
Name: UnitInventoryID, Type: int  
Name: UnitIndicator, Type: varchar(50)  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateUser, Type: varchar(20)


---



### RepairOrderQuoteDetails 

Key: RepairOrderQuoteDetails,  
Type: View,  
Command: vwSR_SSR_RepairOrderQuoteDetails,  
HasReturn: false,  
ReturnType:  
DefaultSort: RepairOrderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: RepairOrderID, Type: int  
Name: RepairOrderTaskID, Type: int  
Name: ROTypeID, Type: varchar(5)  
Name: UnitInventoryID, Type: int  
Name: DetailID, Type: varchar(33)  
Name: PartsInventoryDetailID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: RepairOrderNumber, Type: int  
Name: OwningCustomer, Type: varchar(10)  
Name: OwningCompanyName, Type: varchar(100)  
Name: BillingCustomer, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: TaskNumber, Type: smallint  
Name: UnitNumber, Type: varchar(20)  
Name: UnitStockNumber, Type: varchar(20)  
Name: TransactionType, Type: varchar(13)  
Name: PartType, Type: varchar(4)  
Name: Supplier, Type: varchar(20)  
Name: Item, Type: varchar(50)  
Name: ItemDescription, Type: varchar(50)  
Name: Quantity, Type: int  
Name: CalculatedPrice, Type: decimal  
Name: OverridePrice, Type: decimal  
Name: Price, Type: decimal  
Name: ExtendedPrice, Type: decimal  
Name: ReplacementCost, Type: money  
Name: ExtendedReplacementCost, Type: money  
Name: AverageCost, Type: decimal  
Name: ExtendedAverageCost, Type: decimal  
Name: PartActionFlag, Type: varchar(50)  
Name: EHCCharge, Type: decimal  
Name: ExtendedSellingCost, Type: decimal  
Name: OEMPrice, Type: decimal  
Name: OEMRebateAmount, Type: decimal  
Name: IsInventory, Type: int  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: InsideSalesperson, Type: varchar(20)  
Name: OutsideSalesperson, Type: varchar(20)  
Name: Message, Type: varchar(100)  
Name: ReferenceMPO, Type: varchar(50)  
Name: ControlNumber, Type: varchar(10)  
Name: OverrideTaxStatus, Type: varchar(50)  
Name: FillingBranch, Type: varchar(10)  
Name: BinLocation, Type: varchar(20)  
Name: IsPulled, Type: bit  
Name: IsPartialFill, Type: bit  
Name: IsNoCharge, Type: bit  
Name: BackorderPriority, Type: varchar(50)  
Name: CoreSupplier, Type: varchar(20)  
Name: CorePartNumber, Type: varchar(50)  
Name: CoreDescription, Type: varchar(50)  
Name: CoreClass, Type: varchar(10)  
Name: CorePrice, Type: decimal  
Name: CoreOverridePrice, Type: decimal  
Name: IsCoreNoCharge, Type: bit  
Name: CoreExtendedPrice, Type: money  
Name: CoreCost, Type: money  
Name: IsCoreOneLineTransaction, Type: bit  
Name: CoreReferenceMPO, Type: varchar(50)  
Name: EHCCode, Type: varchar(10)  
Name: EHCDescription, Type: varchar(50)  
Name: IsWarranty, Type: bit  
Name: IsPolicyAdjustment, Type: bit  
Name: PartTechnician, Type: int  
Name: SerialStockType, Type: varchar(50)  
Name: PartStockNumber, Type: varchar(20)  
Name: SerialNumber, Type: varchar(30)  
Name: KitAssemblyTemplate, Type: varchar(1)  
Name: UnitOfMeasure, Type: varchar(10)  
Name: Weight, Type: decimal  
Name: ProductCode, Type: varchar(20)  
Name: Method, Type: varchar(10)  
Name: ProductClass, Type: varchar(50)  
Name: Percentage, Type: decimal  
Name: CalculatedAgainst, Type: varchar(10)


---



### RepairOrderQuoteHeader 

Key: RepairOrderQuoteHeader,  
Type: View,  
Command: vwSR_SSR_RepairOrderQuoteHeader,  
HasReturn: false,  
ReturnType:  
DefaultSort: RepairOrderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: OwningCustomerID, Type: int  
Name: BillingCustomerID, Type: int  
Name: ROTypeID, Type: varchar(5)  
Name: RepairOrderID, Type: int  
Name: UnitInventoryID, Type: int  
Name: StaticPaymentMethodID, Type: int  
Name: UserDefinedPaymentMethodID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: RepairOrderNumber, Type: int  
Name: QuoteStatus, Type: varchar(20)  
Name: QuoteOpenDate, Type: datetime  
Name: QuoteAge, Type: int  
Name: QuoteTaskCount, Type: int  
Name: SalesTaxSetting, Type: varchar(16)  
Name: OriginalRONumber, Type: int  
Name: CustomerBaseBranch, Type: varchar(10)  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: CustomerAccountStatus, Type: varchar(50)  
Name: IsCustomerWarranty, Type: bit  
Name: CustomerIndustryType, Type: varchar(50)  
Name: ContactWorkPhone, Type: varchar(30)  
Name: CustomerPhone, Type: varchar(30)  
Name: ContactName, Type: varchar(201)  
Name: ContactHomePhone, Type: varchar(30)  
Name: CustomerAddress, Type: varchar(201)  
Name: CustomerCity, Type: varchar(100)  
Name: CustomerRegion, Type: varchar(6)  
Name: CustomerPostalCode, Type: varchar(15)  
Name: CustomerEmailAddress, Type: varchar(250)  
Name: FollowUpEmailFlag, Type: bit  
Name: BillingCustomerNumber, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: BillingCustomerAccountStatus, Type: varchar(50)  
Name: IsBillingCustomerWarranty, Type: bit  
Name: BillingCustomerIndustryType, Type: varchar(50)  
Name: BillingCustomerWorkPhone, Type: varchar(30)  
Name: BillingContactName, Type: varchar(201)  
Name: BillingHomePhone, Type: varchar(30)  
Name: BillingCustomerAddress, Type: varchar(201)  
Name: BillingCustomerCity, Type: varchar(100)  
Name: BillingCustomerRegion, Type: varchar(6)  
Name: BillingCustomerPostalCode, Type: varchar(15)  
Name: BillingCustomerCountry, Type: varchar(35)  
Name: BillingCustomerCounty, Type: varchar(35)  
Name: Salesperson, Type: varchar(20)  
Name: AuthorizationNumber, Type: varchar(15)  
Name: UnitNumber, Type: varchar(20)  
Name: UnitVIN, Type: varchar(20)  
Name: UnitCharacteristicType, Type: varchar(20)  
Name: UnitSerialNumber, Type: varchar(20)  
Name: UnitMeterReading, Type: decimal  
Name: UnitMeterType, Type: varchar(50)  
Name: UnitInServiceDate, Type: datetime  
Name: UnitMake, Type: varchar(50)  
Name: UnitModel, Type: varchar(50)  
Name: UnitYear, Type: int  
Name: UnitECMReading, Type: decimal  
Name: TaxStatus, Type: varchar(50)  
Name: TaxBody, Type: varchar(50)  
Name: CreditReserve, Type: decimal  
Name: CustomerPONumber, Type: varchar(30)  
Name: PaymentMethod, Type: varchar(50)  
Name: LPONumber, Type: int  
Name: ArrivalDateTime, Type: datetime  
Name: PromisedDateTime, Type: datetime  
Name: ROPromisedDays, Type: int  
Name: ROPromisedHours, Type: int  
Name: CompletionDate, Type: datetime  
Name: TotalPartsCharges, Type: money  
Name: TotalPartsAverageCost, Type: decimal  
Name: TotalPartsReplacementCost, Type: money  
Name: TotalPartsSellingCost, Type: decimal  
Name: TotalLaborCharges, Type: money  
Name: TotalLaborCost, Type: money  
Name: TotalMiscellaneousCharges, Type: money  
Name: TotalMiscellaneousChargesCost, Type: money  
Name: TotalEHCCharges, Type: decimal  
Name: TotalSalesTax, Type: decimal  
Name: TotalROCharges, Type: decimal  
Name: TotalROAverageCost, Type: decimal  
Name: TotalROReplacementCost, Type: money  
Name: TotalROSellingCost, Type: decimal  
Name: RemoteEstimateID, Type: int  
Name: RemoteApplication, Type: varchar(50)  
Name: ServiceWriter, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime


---



### RepairOrderQuoteTask 

Key: RepairOrderQuoteTask,  
Type: View,  
Command: vwSR_SSR_RepairOrderQuoteTask,  
HasReturn: false,  
ReturnType:  
DefaultSort: RepairOrderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: RepairTypeID, Type: int  
Name: RepairOrderID, Type: int  
Name: RepairOrderTaskID, Type: int  
Name: ROTypeID, Type: varchar(5)  
Name: UnitInventoryID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: RepairOrderNumber, Type: int  
Name: TaskNumber, Type: smallint  
Name: BillingCustomer, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: OwningCustomer, Type: varchar(10)  
Name: OwningCompanyName, Type: varchar(100)  
Name: UnitNumber, Type: varchar(20)  
Name: TaskStatus, Type: varchar(20)  
Name: TaskDepartment, Type: varchar(10)  
Name: OverrideTaxStatus, Type: varchar(50)  
Name: RepairGroup, Type: varchar(10)  
Name: RepairGroupDescription, Type: varchar(50)  
Name: RepairType, Type: varchar(12)  
Name: RepairTypeDescription, Type: varchar(50)  
Name: LaborRateCode, Type: varchar(10)  
Name: LaborRateCodeDescription, Type: varchar(50)  
Name: LaborRate, Type: decimal  
Name: OverrideLaborRate, Type: decimal  
Name: CalculatedLaborRate, Type: decimal  
Name: CallBackDays, Type: int  
Name: BillingHours, Type: decimal  
Name: BookHours, Type: decimal  
Name: IsUseBookHours, Type: bit  
Name: IsAlwaysPayBillingHours, Type: bit  
Name: AlternateBillingCustomer, Type: varchar(10)  
Name: AlternateBillingCompanyName, Type: varchar(100)  
Name: LaborAccounting, Type: varchar(50)  
Name: PartsAccounting, Type: varchar(50)  
Name: PartsQuote, Type: decimal  
Name: PartsActual, Type: money  
Name: PartsTotal, Type: money  
Name: EHCCharges, Type: decimal  
Name: PartsSellingCost, Type: decimal  
Name: PartsAverageCost, Type: decimal  
Name: PartsReplacementCost, Type: money  
Name: LaborQuote, Type: decimal  
Name: LaborTotal, Type: money  
Name: MiscellaneousCharges, Type: money  
Name: MiscellaneousChargesCost, Type: money  
Name: TotalActual, Type: decimal  
Name: TotalPrice, Type: decimal  
Name: TotalSellingCost, Type: decimal  
Name: TotalAverageCost, Type: decimal  
Name: TotalReplacementCost, Type: money  
Name: ComplaintComment, Type: varchar(7500)  
Name: CauseComment, Type: varchar(7500)  
Name: CorrectionComment, Type: varchar(7500)  
Name: VMRSCode, Type: varchar(8000)  
Name: VMRSCodeDescription, Type: varchar(100)  
Name: VMRSTask, Type: varchar(56)  
Name: VMRSFailure, Type: varchar(63)  
Name: VMRSReason, Type: varchar(29)  
Name: SRTCodes, Type: nvarchar(max)  
Name: IsComebackRepair, Type: bit  
Name: ComebackReason, Type: varchar(100)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime


---



### RepairOrderTask 

Key: RepairOrderTask,  
Type: View,  
Command: vwSR_SSR_RepairOrderTask,  
HasReturn: false,  
ReturnType:  
DefaultSort: RONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: Branch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: Department, Type: varchar(10)  
Name: Division, Type: varchar(10)  
Name: RONumber, Type: int  
Name: RepairOrderID, Type: int  
Name: TaskNumber, Type: smallint  
Name: TaskStatus, Type: varchar(50)  
Name: UserDefinedTaskStatus, Type: varchar(20)  
Name: TaskDepartment, Type: varchar(10)  
Name: TaskRepairType, Type: varchar(12)  
Name: RepairTypeID, Type: int  
Name: TaskRepairTypeDescription, Type: varchar(50)  
Name: TaskRepairGroup, Type: varchar(10)  
Name: TaskRepairGroupDescription, Type: varchar(50)  
Name: TaskSRTCode, Type: nvarchar(max)  
Name: TaskComplaintComment, Type: varchar(7500)  
Name: TaskCorrectionComment, Type: varchar(7500)  
Name: TaskCauseComment, Type: varchar(7500)  
Name: TaskBillingType, Type: varchar(25)  
Name: AlternateBillingCustomer, Type: varchar(10)  
Name: AlternateBillingCompanyName, Type: varchar(100)  
Name: TaskBillingHours, Type: decimal  
Name: TaskBookHours, Type: decimal  
Name: TaskLaborQuote, Type: decimal  
Name: TaskLaborRate, Type: decimal  
Name: TaskDefaultLaborRate, Type: decimal  
Name: TaskOverrideLaborRate, Type: decimal  
Name: TaskPartsQuote, Type: decimal  
Name: TaskMiscellaneousChargesQuote, Type: decimal  
Name: TaskCloseDate, Type: datetime  
Name: IsTaskAComebackRepair, Type: bit  
Name: IsTaskCompleted, Type: bit  
Name: IsTaskClockedON, Type: bit  
Name: IsTaskWaiting, Type: bit  
Name: IsTaskWaitingForParts, Type: bit  
Name: WasTaskWaitingForParts, Type: int  
Name: TaskTechnicians, Type: nvarchar(max)  
Name: TaskClockedOnTechnicians, Type: nvarchar(max)  
Name: TaskHoursWorked, Type: decimal  
Name: TaskHoursBilled, Type: decimal  
Name: TaskTotalParts, Type: money  
Name: TaskPartsActual, Type: money  
Name: TaskEHCCharge, Type: decimal  
Name: TaskTotalLabor, Type: money  
Name: TaskLaborCost, Type: money  
Name: TaskLaborActual, Type: money  
Name: TaskPartsReplacementCost, Type: money  
Name: TaskMiscellaneousCharges, Type: money  
Name: TaskMiscellaneousChargesCost, Type: money  
Name: TaskTotal, Type: decimal  
Name: TaskTotalActual, Type: decimal  
Name: TaskTotalCost, Type: money  
Name: TaskEffectiveLaborRate, Type: decimal  
Name: TaskPerformance, Type: decimal  
Name: TaskOpenTime, Type: decimal  
Name: TaskRemainingHours, Type: decimal  
Name: TaskTotalTimeWorked, Type: decimal  
Name: TaskAdjustmentTime, Type: decimal  
Name: TaskComebackReason, Type: varchar(100)  
Name: ROUniqueID, Type: int  
Name: TaskPartsSellingCost, Type: decimal  
Name: TaskPartsAverageCost, Type: decimal  
Name: TaskTotalSellingCost, Type: decimal  
Name: TaskTotalAverageCost, Type: decimal  
Name: TaskTotalReplacementCost, Type: money  
Name: RepairOrderTaskID, Type: int  
Name: ROTypeID, Type: varchar(7)  
Name: RepairOrderInvoiceID, Type: int  
Name: HeaderJoinID, Type: int  
Name: TaskJoinID, Type: int  
Name: TaskLastUpdateDate, Type: datetime  
Name: TaskAddDate, Type: datetime  
Name: TaskLastUpdateUser, Type: varchar(20)  
Name: TaskAddUser, Type: varchar(20)  
Name: TaskCallBackDays, Type: int  
Name: TaskLaborRateCode, Type: varchar(10)  
Name: TaskLaborRateDescription, Type: varchar(50)  
Name: TaskOverrideTaxStatus, Type: varchar(50)  
Name: TaskPartsAccounting, Type: varchar(50)  
Name: TaskLaborAccounting, Type: varchar(50)  
Name: TaskUseBookHours, Type: bit  
Name: VMRSCode, Type: varchar(8000)  
Name: VMRSCodeDescription, Type: varchar(100)  
Name: VMRSTask, Type: varchar(56)  
Name: VMRSFailure, Type: varchar(63)  
Name: VMRSReason, Type: varchar(29)  
Name: TaskAlwaysPayBillingHours, Type: bit  
Name: InvoiceNumber, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: UnitNumber, Type: varchar(20)  
Name: UnitInventoryID, Type: int  
Name: OwningCompanyName, Type: varchar(100)  
Name: OwningCustomer, Type: varchar(10)  
Name: BillToCompanyName, Type: varchar(100)  
Name: BillToCustomer, Type: varchar(10)


---



### RepairTypes 

Key: RepairTypes,  
Type: View,  
Command: vwSR_SSR_RepairTypes,  
HasReturn: false,  
ReturnType:  
DefaultSort: RepairType,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: RepairType, Type: varchar(12)  
Name: RepairTypeID, Type: int  
Name: RepairGroupID, Type: int  
Name: RepairTypeDescription, Type: varchar(50)  
Name: IsNonBillable, Type: bit  
Name: PrintPartsDetail, Type: bit  
Name: PrintLaborDetail, Type: bit  
Name: PrintTaskSubtotals, Type: bit  
Name: PrintTechnician, Type: bit  
Name: PrintAllMiscChargeDetail, Type: bit  
Name: BillingHours, Type: decimal  
Name: BookHours, Type: decimal  
Name: CallBackdays, Type: int  
Name: PartsQuoteType, Type: varchar(51)  
Name: PartsQuote, Type: decimal  
Name: LaborQuoteType, Type: varchar(51)  
Name: LaborQuote, Type: decimal  
Name: PayOnlyGreaterIncentive, Type: bit  
Name: AlwaysPayIncentive, Type: bit  
Name: InActive, Type: bit  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: RepairGroupMaximumComebackDays, Type: int  
Name: RepairGroupPerformComebackCheck, Type: bit  
Name: PerformComebackCheck, Type: bit  
Name: MaximumComebackDays, Type: int  
Name: NoAutoCharges, Type: bit  
Name: PrintTasktotalOnly, Type: bit  
Name: RepairGroupDescription, Type: varchar(50)  
Name: RepairGroup, Type: varchar(10)  
Name: LaborRateCode, Type: varchar(10)  
Name: OverrideTaxStatus, Type: varchar(50)  
Name: WorkMixCategory, Type: varchar(17)  
Name: ComplaintComment, Type: varchar(7500)  
Name: CauseComment, Type: varchar(7500)  
Name: CorrectionComment, Type: varchar(7500)  
Name: VMRSCode, Type: int  
Name: VMRSCodeDescription, Type: varchar(100)  
Name: VMRSTask, Type: varchar(50)

## Repair Order



---



### RepairOrderDetails 

Key: RepairOrderDetails,  
Type: View,  
Command: vwSV_SSR_RepairOrderDetails,  
HasReturn: false,  
ReturnType:  
DefaultSort: RONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: Branch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: Division, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: RONumber, Type: int  
Name: RepairOrderID, Type: int  
Name: RepairOrderInvoiceID, Type: int  
Name: ROStatus, Type: varchar(20)  
Name: DateInvoiced, Type: datetime  
Name: InvoiceNumber, Type: varchar(50)  
Name: TransactionType, Type: varchar(13)  
Name: Supplier, Type: varchar(50)  
Name: Item, Type: varchar(50)  
Name: PartType, Type: varchar(4)  
Name: TechnicianNumber, Type: int  
Name: ItemDescription, Type: varchar(203)  
Name: QuantityHours, Type: decimal  
Name: CalculatedPrice, Type: decimal  
Name: Price, Type: decimal  
Name: Extended Price, Type: decimal  
Name: OverridePrice, Type: decimal  
Name: ReplacementCost, Type: money  
Name: ExtendedReplacementCost, Type: money  
Name: AverageCost, Type: decimal  
Name: ExtendedAverageCost, Type: decimal  
Name: PartActionFlag, Type: varchar(50)  
Name: IsBillingAdjustment, Type: bit  
Name: OTHours, Type: decimal  
Name: OTMultiplier, Type: decimal  
Name: BillCustomerOT, Type: bit  
Name: TimeIn, Type: datetime  
Name: TimeOut, Type: datetime  
Name: Shift, Type: varchar(10)  
Name: EHCCharge, Type: decimal  
Name: ExtendedSellingCost, Type: decimal  
Name: RepairOrderTaskID, Type: int  
Name: TaskNumber, Type: smallint  
Name: OEMPrice, Type: decimal  
Name: OEMRebateAmount, Type: decimal  
Name: IsInventory, Type: int  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: ROTypeID, Type: varchar(7)  
Name: HeaderJoinID, Type: int  
Name: TaskJoinID, Type: int  
Name: DetailID, Type: varchar(33)  
Name: UnitNumber, Type: varchar(20)  
Name: StockNumber, Type: varchar(20)  
Name: InsideSalesperson, Type: varchar(50)  
Name: OutsideSalesperson, Type: varchar(50)  
Name: Message, Type: varchar(100)  
Name: ReferenceMPO, Type: varchar(50)  
Name: ControlNumber, Type: varchar(10)  
Name: OverrideTaxStatus, Type: varchar(50)  
Name: FillingBranch, Type: varchar(10)  
Name: BinLocation, Type: varchar(50)  
Name: IsPulled, Type: bit  
Name: IsPartialFill, Type: bit  
Name: IsNoCharge, Type: bit  
Name: BackorderPriority, Type: varchar(50)  
Name: CoreSupplier, Type: varchar(50)  
Name: CorePartNumber, Type: varchar(50)  
Name: CoreDescription, Type: varchar(50)  
Name: CoreClass, Type: varchar(10)  
Name: CorePrice, Type: decimal  
Name: CoreOverridePrice, Type: decimal  
Name: IsCoreNoCharge, Type: bit  
Name: CoreExtendedPrice, Type: money  
Name: CoreCost, Type: money  
Name: IsCoreOneLineTransaction, Type: bit  
Name: CoreReferenceMPO, Type: varchar(50)  
Name: EHCCode, Type: varchar(10)  
Name: EHCDescription, Type: varchar(50)  
Name: IsWarranty, Type: bit  
Name: IsPolicyAdjustment, Type: bit  
Name: PartTechnician, Type: int  
Name: SerialStockType, Type: varchar(50)  
Name: PartStockNumber, Type: varchar(20)  
Name: SerialNumber, Type: varchar(30)  
Name: KitAssemblyTemplate, Type: varchar(1)  
Name: UnitOfMeasure, Type: varchar(10)  
Name: Weight, Type: decimal  
Name: ProductCode, Type: varchar(20)  
Name: RepairGroup, Type: varchar(50)  
Name: RepairType, Type: varchar(50)  
Name: IsEnterLaborInTotalHours, Type: bit  
Name: OTDescription, Type: varchar(50)  
Name: OTHourlyCost, Type: money  
Name: RateLevelDescription, Type: varchar(42)  
Name: OTHourlyRate, Type: decimal  
Name: OTBillingTotal, Type: decimal  
Name: Method, Type: varchar(10)  
Name: ProductClass, Type: varchar(50)  
Name: Percentage, Type: decimal  
Name: CalculatedAgainst, Type: varchar(10)  
Name: OwningCustomer, Type: varchar(10)  
Name: OwningCompanyName, Type: varchar(100)  
Name: BillingCustomer, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: PartsInventoryDetailID, Type: int  
Name: UnitInventoryID, Type: int


---



### RepairOrderHeader 

Key: RepairOrderHeader,  
Type: View,  
Command: vwSV_SSR_RepairOrderHeader,  
HasReturn: false,  
ReturnType:  
DefaultSort: RONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: CustomerID, Type: int  
Name: BillingCustomerID, Type: int  
Name: RepairOrderID, Type: int  
Name: RepairOrderInvoiceID, Type: int  
Name: Division, Type: varchar(100)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: RONumber, Type: int  
Name: RODateInvoiced, Type: datetime  
Name: InvoiceNumber, Type: varchar(50)  
Name: RODaysCompletedToInvoiced, Type: int  
Name: InvoiceUser, Type: varchar(20)  
Name: ROStatus, Type: varchar(20)  
Name: RODateOpened, Type: datetime  
Name: SalesTaxSetting, Type: varchar(16)  
Name: CustomerBaseBranch, Type: varchar(10)  
Name: CustomerNumber, Type: varchar(10)  
Name: CustomerName, Type: varchar(100)  
Name: CustomerAccountStatus, Type: varchar(50)  
Name: IsCustomerWarranty, Type: bit  
Name: CustomerPhone, Type: varchar(30)  
Name: ContactName, Type: varchar(201)  
Name: ContactWorkPhone, Type: varchar(30)  
Name: ContactHomePhone, Type: varchar(30)  
Name: CustomerAddress, Type: varchar(201)  
Name: CustomerCity, Type: varchar(100)  
Name: CustomerRegion, Type: varchar(6)  
Name: CustomerPostalCode, Type: varchar(15)  
Name: EmailAddressOfCustomer, Type: varchar(250)  
Name: FollowUpEmailFlag, Type: bit  
Name: BillingCustomerNumber, Type: varchar(10)  
Name: BillingCustomerName, Type: varchar(100)  
Name: BillingCustomerAccountStatus, Type: varchar(50)  
Name: IsBillingCustomerWarranty, Type: bit  
Name: BillingCustomerWorkPhone, Type: varchar(30)  
Name: BillingContactname, Type: varchar(201)  
Name: BillingHomePhone, Type: varchar(30)  
Name: Salesperson, Type: varchar(20)  
Name: AuthorizationNumber, Type: varchar(15)  
Name: InvoiceDueDate, Type: datetime  
Name: BillingCustomerAddress, Type: varchar(201)  
Name: BillingCustomerCity, Type: varchar(100)  
Name: BillingCustomerRegion, Type: varchar(6)  
Name: BillingCustomerPostalCode, Type: varchar(15)  
Name: BillingCustomerCountry, Type: varchar(35)  
Name: BillingCustomerCounty, Type: varchar(35)  
Name: CustomerUnitNumber, Type: varchar(20)  
Name: VIN, Type: varchar(30)  
Name: UnitMeterReading, Type: decimal  
Name: MeterType, Type: varchar(50)  
Name: InServiceDate, Type: datetime  
Name: UnitMake, Type: varchar(50)  
Name: UnitModel, Type: varchar(50)  
Name: UnitYear, Type: int  
Name: ECMReading, Type: decimal  
Name: TaxStatus, Type: varchar(50)  
Name: TaxBody, Type: varchar(50)  
Name: CreditReserve, Type: decimal  
Name: RO Customer PO Number, Type: varchar(30)  
Name: PaymentMethod, Type: varchar(50)  
Name: LPONumber, Type: int  
Name: ROArrivalDateTime, Type: datetime  
Name: ROPromiseDateTime, Type: datetime  
Name: RODateCompleted, Type: datetime  
Name: ROPartsCharges, Type: money  
Name: ROPartsReplacementCost, Type: money  
Name: ROPartsSellingCost, Type: decimal  
Name: ROPartsAverageCost, Type: decimal  
Name: ROLaborCharges, Type: money  
Name: ROLaborCost, Type: money  
Name: ROMiscellaneousCharges, Type: money  
Name: ROMiscellaneousChargesCost, Type: money  
Name: ROEHCCharges, Type: decimal  
Name: SalesTaxTotal, Type: decimal  
Name: TotalROCharges, Type: decimal  
Name: IndustryType, Type: varchar(50)  
Name: UnitSerialNumber, Type: varchar(20)  
Name: CharacteristicType, Type: varchar(20)  
Name: OriginalRONumber, Type: int  
Name: ROAge, Type: int  
Name: ROPromisedDays, Type: int  
Name: ROPromisedHours, Type: int  
Name: UserROStatus, Type: varchar(20)  
Name: IsROCompleted, Type: bit  
Name: IsROWaiting, Type: bit  
Name: IsROClockedON, Type: bit  
Name: IsROWaitingForParts, Type: bit  
Name: ROServiceWriter, Type: varchar(20)  
Name: RODaysSinceLastWorkedOn, Type: int  
Name: ROHoursSinceLastWorkedOn, Type: int  
Name: ROHoursWorked, Type: decimal  
Name: ROOpenTime, Type: decimal  
Name: RORemainingHours, Type: decimal  
Name: ROPerformance, Type: decimal  
Name: ROBillingHours, Type: decimal  
Name: ROHoursBilled, Type: decimal  
Name: ROTaskCount, Type: int  
Name: ROWaitingTasksCount, Type: int  
Name: ROBookHours, Type: decimal  
Name: ROTechnicians, Type: nvarchar(max)  
Name: ROClockedONTechnicians, Type: nvarchar(max)  
Name: ROUniqueID, Type: int  
Name: ROTotalSellingCost, Type: decimal  
Name: ROTotalAverageCost, Type: decimal  
Name: RO Total Replacement Cost, Type: money  
Name: IsVoided, Type: bit  
Name: RemoteEstimateID, Type: int  
Name: RemoteApplication, Type: varchar(50)  
Name: CompletedToInvoicedInterval, Type: varchar(10)  
Name: UnitInventoryID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: AddDate, Type: datetime  
Name: ROTypeID, Type: varchar(7)  
Name: HeaderJoinID, Type: int  
Name: UserDefinedPaymentMethodID, Type: int  
Name: StaticPaymentMethodID, Type: int  
Name: BillingCustomerIndustryType, Type: varchar(50)  
Name: DaysArrivalToFirstPunch, Type: int  
Name: DaysOpenToFirstPunch, Type: int  
Name: DaysFirstPunchToLastPunch, Type: int  
Name: FirstPunchDate, Type: datetime  
Name: LastPunchDate, Type: datetime  
Name: RepairOrderStatusID, Type: int

## Technician



---



### Technician 

Key: Technician,  
Type: View,  
Command: vwSR_SSR_Technician,  
HasReturn: false,  
ReturnType:  
DefaultSort: TechnicianNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: TechnicianID, Type: int  
Name: TechnicianNumber, Type: int  
Name: Inactive, Type: bit  
Name: IsFlatRate, Type: bit  
Name: IsPayIncentive, Type: bit  
Name: DoNotPayOvertime, Type: bit  
Name: TechnicianName, Type: varchar(201)  
Name: TechnicianBaseBranch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: TechnicianBaseDepartment, Type: varchar(10)  
Name: DepartmentID, Type: int  
Name: TechnicianBaseShift, Type: varchar(50)  
Name: HireDate, Type: datetime  
Name: ReviewDate, Type: datetime  
Name: RatePerHour, Type: decimal  
Name: ShiftPremium, Type: decimal  
Name: ShiftID, Type: int  
Name: HoursPerDayBeforeOT, Type: decimal  
Name: HoursPerWeekBeforeOT, Type: decimal  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: IsTechnicianAvailable, Type: int  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateUser, Type: varchar(20)


---



### TechnicianCertification 

Key: TechnicianCertification,  
Type: View,  
Command: vwSR_SSR_TechnicianCertification,  
HasReturn: false,  
ReturnType:  
DefaultSort: [Technician Number],  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: Technician Number, Type: int  
Name: Technician Name, Type: varchar(203)  
Name: Tech Certification Number, Type: varchar(50)  
Name: Certification Date, Type: datetime  
Name: Certification Expiration Date, Type: datetime  
Name: Certification Type, Type: varchar(50)  
Name: Certification Description, Type: varchar(100)  
Name: Is Permit, Type: int  
Name: Print On Invoice, Type: int  
Name: IsPermit, Type: bit  
Name: IsPrintOnInvoice, Type: bit  
Name: Add User, Type: varchar(20)  
Name: Update User, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime


---



### TechnicianPerformance 

Key: TechnicianPerformance,  
Type: View,  
Command: vwSR_SSR_TechnicianPerformance,  
HasReturn: false,  
ReturnType:  
DefaultSort: TechnicianNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: RepairGroupID, Type: int  
Name: ContactID, Type: int  
Name: TechnicianID, Type: int  
Name: TechnicianNumber, Type: int  
Name: TechnicianUserName, Type: varchar(20)  
Name: TechnicianName, Type: varchar(203)  
Name: PaidFlatRate, Type: bit  
Name: PaidIncentive, Type: bit  
Name: Inactive, Type: bit  
Name: TechnicianBaseBranch, Type: varchar(10)  
Name: TechnicianBaseDepartment, Type: varchar(10)  
Name: TechnicianBaseShift, Type: varchar(50)  
Name: HireDate, Type: datetime  
Name: ReviewDate, Type: datetime  
Name: RepairGroup, Type: varchar(10)  
Name: RepairGroupDescription, Type: varchar(50)  
Name: BeginningCalculationDate, Type: datetime  
Name: LastCalculationDate, Type: datetime  
Name: ProductivityPercentage, Type: decimal  
Name: ProductivityFreezeThruDate, Type: datetime  
Name: EfficiencyPercentage, Type: decimal  
Name: EfficiencyFreezeThruDate, Type: datetime  
Name: GainLossPercentage, Type: decimal  
Name: GainLossFreezeThruDate, Type: datetime  
Name: ProficiencyPercentage, Type: decimal  
Name: ProficiencyFreezeThruDate, Type: datetime  
Name: ComebackHours, Type: decimal  
Name: EffectiveLaborRate, Type: decimal


---



### TechnicianProductivity 

Key: TechnicianProductivity,  
Type: View,  
Command: vwSR_SSR_TechnicianProductivity,  
HasReturn: false,  
ReturnType:  
DefaultSort: TechnicianNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: TechnicianID, Type: int  
Name: TechnicianNumber, Type: int  
Name: Inactive, Type: bit  
Name: TechnicianName, Type: varchar(203)  
Name: TechnicianBaseBranch, Type: varchar(10)  
Name: TechnicianBaseDepartment, Type: varchar(10)  
Name: TechnicianBaseShift, Type: varchar(50)  
Name: MonthNumber, Type: int  
Name: Month, Type: varchar(3)  
Name: Year, Type: int  
Name: ProductiveHours, Type: decimal  
Name: NonProductiveHours, Type: decimal  
Name: BilledHours, Type: decimal  
Name: TotalWorkedHours, Type: decimal  
Name: ProductivityPercentage, Type: decimal  
Name: EfficiencyPercentage, Type: decimal  
Name: GainLossPercentage, Type: decimal  
Name: ProficiencyPercentage, Type: decimal  
Name: EffectiveRate, Type: decimal  
Name: ComebackHours, Type: decimal


---



### TechnicianTime 

Key: TechnicianTime,  
Type: View,  
Command: vwSR_SSR_TechnicianTime,  
HasReturn: false,  
ReturnType:  
DefaultSort: TechnicianNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: TimeID, Type: int  
Name: RepairOrderID, Type: int  
Name: RepairOrderTaskID, Type: int  
Name: TechnicianID, Type: int  
Name: ShiftID, Type: int  
Name: RepairOrderLaborInvoiceID, Type: int  
Name: RepairTypeID, Type: int  
Name: RepairGroupID, Type: int  
Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: OriginalRepairOrderID, Type: int  
Name: RepairOrderStatusID, Type: int  
Name: RepairTaskStatusID, Type: int  
Name: LaborRateCodeID, Type: int  
Name: LaborQuoteTypeID, Type: int  
Name: OwningCustomerID, Type: int  
Name: BillingCustomerID, Type: int  
Name: AddUserID, Type: int  
Name: UpdateUserID, Type: int  
Name: AddApplicationID, Type: int  
Name: UpdateApplicationID, Type: int  
Name: TechnicianNumber, Type: int  
Name: TechnicianFirstName, Type: varchar(100)  
Name: TechnicianLastName, Type: varchar(100)  
Name: TechnicianName, Type: varchar(201)  
Name: BranchCode, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: Shift, Type: varchar(10)  
Name: RepairOrderNumber, Type: varchar(30)  
Name: OriginalRepairOrder, Type: varchar(30)  
Name: IsSecondaryRO, Type: bit  
Name: TaskNumber, Type: smallint  
Name: InvoiceNumber, Type: varchar(50)  
Name: Invoiced, Type: bit  
Name: OwningCustomer, Type: varchar(10)  
Name: OwningCompanyName, Type: varchar(100)  
Name: BillingCustomer, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: RepairGroup, Type: varchar(10)  
Name: RepairGroupDescription, Type: varchar(50)  
Name: RepairType, Type: varchar(12)  
Name: RepairTypeDescription, Type: varchar(50)  
Name: IsNonBillable, Type: bit  
Name: RepairOrderStatus, Type: varchar(20)  
Name: RepairTaskStatus, Type: varchar(50)  
Name: BillingHours, Type: decimal  
Name: UseBookHours, Type: bit  
Name: LaborQuote, Type: decimal  
Name: LaborRateCode, Type: varchar(10)  
Name: LaborRate, Type: decimal  
Name: IsEnterLaborInTotalHours, Type: bit  
Name: BarcodeDateIn, Type: datetime  
Name: BarcodeTimeIn, Type: datetime  
Name: BarcodeDateOut, Type: datetime  
Name: BarcodeTimeOut, Type: datetime  
Name: TotalHours, Type: decimal  
Name: TotalHoursLessBillingAdjustments, Type: decimal  
Name: HoursBilled, Type: decimal  
Name: NBTotalHours, Type: decimal  
Name: HoursWorked, Type: decimal  
Name: CombinedTotalHours, Type: decimal  
Name: Price, Type: decimal  
Name: Cost, Type: money  
Name: ExtendedPrice, Type: money  
Name: ExtendedCost, Type: money  
Name: NBExtendedCost, Type: money  
Name: OT_BillCustomer, Type: bit  
Name: OT_RateLevelParamNum, Type: int  
Name: OTHourlyRate, Type: decimal  
Name: OTBillingTotal, Type: decimal  
Name: OT_TotalHours, Type: decimal  
Name: NBOT_TotalHours, Type: decimal  
Name: OT_RateMultLevelParamNum, Type: int  
Name: OT_RateMultiplier, Type: decimal  
Name: OT_Cost, Type: money  
Name: TotalOTCost, Type: decimal  
Name: NBOT_TotalCost, Type: decimal  
Name: IsInOutTime, Type: bit  
Name: IsBillingAdjustment, Type: bit  
Name: IsCompleted, Type: bit  
Name: IsWarrantyTransaction, Type: bit  
Name: IsPolicyAdjustmentTransaction, Type: bit  
Name: IsBase, Type: bit  
Name: IsSubmittedforPayroll, Type: bit  
Name: IsPayrollProcessed, Type: bit  
Name: IsManuallyUpdated, Type: bit  
Name: AddApplicationNumber, Type: varchar(10)  
Name: AddApplication, Type: varchar(75)  
Name: UpdateApplicationNumber, Type: varchar(10)  
Name: UpdateApplication, Type: varchar(75)  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdate, Type: datetime  
Name: GainLoss, Type: int  
Name: GainLossDetail, Type: int  
Name: HoursPaid, Type: decimal  
Name: IntOriginalRepairOrder, Type: int  
Name: IntRepairOrderNumber, Type: int  
Name: OT_IsRate, Type: bit  
Name: RecordSource, Type: int  
Name: Team, Type: int

## Service Unit



---



### Unit

Key: Unit,  
Type: View,  
Command: vwSR_SSR_Unit,  
HasReturn: false,  
ReturnType:  
DefaultSort: UnitNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: StockNumber, Type: varchar(20)  
Name: Year, Type: int  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: Manufacturer, Type: varchar(50)  
Name: VIN, Type: varchar(20)  
Name: SerialNumber, Type: varchar(20)  
Name: Barcode, Type: varchar(40)  
Name: CharacteristicType, Type: varchar(20)  
Name: AvailabilityStatus, Type: varchar(50)  
Name: SellingStatus, Type: varchar(50)  
Name: ControlBranch, Type: varchar(10)  
Name: BookBranch, Type: varchar(100)  
Name: ControlDepartment, Type: varchar(10)  
Name: InventoryType, Type: varchar(50)  
Name: NewUnit, Type: bit  
Name: Export, Type: bit  
Name: TradeInAllowance, Type: decimal  
Name: ActualCashValue, Type: decimal  
Name: CurrencyCode, Type: varchar(10)  
Name: UnitCostConversion, Type: varchar(50)  
Name: UnitCostConverted, Type: bit  
Name: ListPrice, Type: decimal  
Name: AskingPrice, Type: decimal  
Name: LowPrice, Type: decimal  
Name: SpecialPrice, Type: decimal  
Name: SpecialPriceExpiration, Type: varchar(30)  
Name: ProductClass, Type: varchar(50)  
Name: FETCharged, Type: bit  
Name: TireTaxCredit, Type: decimal  
Name: FETExemptDeliveryExpenses, Type: decimal  
Name: FETExemptEquipment, Type: decimal  
Name: AcquisitionMethod, Type: varchar(50)  
Name: Consignor, Type: varchar(100)  
Name: AcquisitionDate, Type: datetime  
Name: AcquiringSalesperson, Type: varchar(20)  
Name: PODealCustomerName, Type: varchar(100)  
Name: PODealCustomer, Type: varchar(10)  
Name: POBranch, Type: varchar(10)  
Name: PODepartment, Type: varchar(10)  
Name: PONumber, Type: int  
Name: FactoryOrderNumber, Type: varchar(20)  
Name: PurchaseOrderStatus, Type: varchar(50)  
Name: OrderDate, Type: datetime  
Name: VoidOrderDate, Type: datetime  
Name: BuildDate, Type: datetime  
Name: RequestShipDate, Type: datetime  
Name: ActualShipDate, Type: datetime  
Name: EstimatedArrivalDate, Type: datetime  
Name: ReceiveInvoiceDate, Type: datetime  
Name: ReceiveInvoiceNumber, Type: varchar(20)  
Name: ReceivedDate, Type: datetime  
Name: DaysInInventoryReceiveDate, Type: int  
Name: DaysInInventoryReceiveInvoiceDate, Type: int  
Name: DaysInInventory, Type: int  
Name: PreviousOwner, Type: varchar(50)  
Name: ReplenishStock, Type: bit  
Name: CurrentTitleNumber, Type: varchar(30)  
Name: TitleRegion, Type: varchar(6)  
Name: UsageType, Type: varchar(20)  
Name: GVWR, Type: int  
Name: MeterType, Type: varchar(50)  
Name: CurrentMeterReading, Type: decimal  
Name: CurrentMeterReadingDate, Type: datetime  
Name: CurrentECMReading, Type: decimal  
Name: CurrentECMReadingDate, Type: datetime  
Name: LocationBranch, Type: varchar(10)  
Name: LotLocation, Type: varchar(20)  
Name: TemporaryLocationType, Type: varchar(50)  
Name: TemporaryLocationName, Type: varchar(100)  
Name: InServiceDealerCode, Type: varchar(20)  
Name: InServiceDate, Type: datetime  
Name: InServiceMeterReading, Type: decimal  
Name: WarrantyMeter, Type: decimal  
Name: PeriodType, Type: varchar(50)  
Name: WarrantyPeriod, Type: int  
Name: WarrantyContract, Type: varchar(50)  
Name: SoldCustomerKey, Type: varchar(10)  
Name: SoldCustomerName, Type: varchar(100)  
Name: SoldCustomerAddress1, Type: varchar(100)  
Name: SoldCustomerAddress2, Type: varchar(100)  
Name: SoldCustomerCity, Type: varchar(100)  
Name: SoldCustomerRegion, Type: varchar(6)  
Name: SoldCustomerPostalCode, Type: varchar(15)  
Name: SoldCustomerCountry, Type: varchar(50)  
Name: SoldCustomerCounty, Type: varchar(50)  
Name: SoldDate, Type: datetime  
Name: SoldInvoiceNumber, Type: varchar(20)  
Name: SoldPrice, Type: decimal  
Name: SoldCost, Type: money  
Name: SoldSalesperson, Type: varchar(20)  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: IsActiveUnit, Type: bit  
Name: BaseCost, Type: money  
Name: PurchaseCost, Type: money  
Name: Inactive, Type: bit  
Name: CurrentCost, Type: decimal  
Name: OpenLpos, Type: decimal  
Name: TotalUnitCost, Type: decimal  
Name: FlooringBalance, Type: decimal  
Name: UnitInventoryID, Type: int  
Name: UnitNumber, Type: varchar(20)  
Name: DueForServiceBranch, Type: varchar(10)  
Name: UnitIndicator, Type: varchar(50)  
Name: FleetType, Type: varchar(50)  
Name: EquipmentType, Type: varchar(50)  
Name: EquipmentClass, Type: varchar(50)  
Name: BillingMeterReading, Type: decimal  
Name: BillingMeterReadingDate, Type: datetime


---



### UnitComponents 

Key: UnitComponents,  
Type: View,  
Command: vwSR_SSR_UnitComponents,  
HasReturn: false,  
ReturnType:  
DefaultSort: UnitNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: ComponentID, Type: int  
Name: UnitNumber, Type: varchar(20)  
Name: UnitInventoryID, Type: int  
Name: UnitIndicator, Type: varchar(50)  
Name: Description, Type: varchar(50)  
Name: ComponentTypeID, Type: int  
Name: ComponentName, Type: varchar(50)  
Name: ComponentManufacturer, Type: varchar(50)  
Name: ComponentManufacturerID, Type: int  
Name: ComponentModel, Type: varchar(50)  
Name: ComponentModelID, Type: int  
Name: SerialNumber, Type: varchar(20)  
Name: InServiceDate, Type: datetime  
Name: ComponentDeactivateDate, Type: datetime  
Name: PartNumber, Type: varchar(50)  
Name: MeterType, Type: varchar(50)  
Name: MeterTypeID, Type: int  
Name: WarrantyMeter, Type: decimal  
Name: WarrantyPeriod, Type: int  
Name: WarrantyPeriodType, Type: varchar(50)  
Name: WarrantyPeriodTypeID, Type: int  
Name: WarrantyContract, Type: varchar(50)  
Name: WarrantyPartPercentage, Type: decimal  
Name: WarrantyLaborPercentage, Type: decimal  
Name: Deductible, Type: decimal  
Name: DeactivateRepairOrderNumber, Type: int  
Name: DeactivateRepairOrderID, Type: int  
Name: DeactivateRepairOrderTask, Type: smallint  
Name: DeactivateRepairOrderTaskID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddUserID, Type: int  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: UpdateUserID, Type: int  
Name: LastUpdate, Type: datetime  
Name: IsActiveUnit, Type: bit  
Name: CurrentMeterReadingDate, Type: datetime  
Name: CurrentMeterReading, Type: decimal


---



### UnitOwningCustomer 

Key: UnitOwningCustomer,  
Type: View,  
Command: vwSR_SSR_UnitOwningCustomer,  
HasReturn: false,  
ReturnType:  
DefaultSort: UnitNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: UnitInventoryID, Type: int  
Name: CustomerID, Type: int  
Name: EntityTypeID, Type: int  
Name: BillToTypeID, Type: int  
Name: ShipToTypeID, Type: int  
Name: UnitNumber, Type: varchar(20)  
Name: Inactive, Type: bit  
Name: Year, Type: int  
Name: Make, Type: varchar(50)  
Name: Model, Type: varchar(50)  
Name: Manufacturer, Type: varchar(50)  
Name: VIN, Type: varchar(20)  
Name: CharacteristicType, Type: varchar(20)  
Name: CustomerBaseBranch, Type: varchar(10)  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: IndustryType, Type: varchar(50)  
Name: OutsidePartsSalesperson, Type: varchar(50)  
Name: OutsideServiceSalesperson, Type: varchar(50)  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)

## Parts



---   ### CustomerCoreRighttoReturn 

Key: CustomerCoreRighttoReturn,  
Type: View,  
Command: vwIN_SSR_CustomerCoreRighttoReturn,  
HasReturn: false,  
ReturnType:  
DefaultSort: CustomerNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: RightToReturnID, Type: int  
Name: CustomerID, Type: int  
Name: SalesOrderID, Type: int  
Name: RepairOrderID, Type: int  
Name: AddUserID, Type: int  
Name: UpdateUserID, Type: int  
Name: BranchID, Type: int  
Name: PartsInventoryID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: SupplierID, Type: int  
Name: Branch, Type: varchar(10)  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: SalesOrderNumber, Type: int  
Name: RepairOrderNumber, Type: int  
Name: InvoiceNumber, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: PartNumber, Type: varchar(50)  
Name: Supplier, Type: varchar(20)  
Name: PartDescription, Type: varchar(50)  
Name: MaximumPrice, Type: decimal  
Name: Quantity, Type: int  
Name: SoldDate, Type: datetime  
Name: IsNoCharge, Type: bit  
Name: ExpirationDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime


---



### CustomerPurchasesandReturns 

Key: CustomerPurchasesandReturns,  
Type: View,  
Command: vwIN_SSR_CustomerPurchasesandReturns,  
HasReturn: false,  
ReturnType:  
DefaultSort: Customer,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: CustomerPurchasesReturnsSearchID, Type: int  
Name: OrderType, Type: varchar(14)  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(50)  
Name: CustomerID, Type: int  
Name: Customer, Type: varchar(50)  
Name: CompanyName, Type: varchar(100)  
Name: InvoiceNumber, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: IsVoided, Type: bit  
Name: OrderDetailID, Type: int  
Name: OrderDetailInvoiceID, Type: int  
Name: OrderID, Type: int  
Name: OrderInvoiceID, Type: int  
Name: SupplierID, Type: int  
Name: Supplier, Type: varchar(50)  
Name: PartsInventoryID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: PartNumber, Type: varchar(50)  
Name: PartDescription, Type: varchar(50)  
Name: ReplacementCost, Type: decimal  
Name: AverageCost, Type: decimal  
Name: Price, Type: decimal  
Name: Quantity, Type: int  
Name: ExtendedPrice, Type: decimal  
Name: ItemTypeID, Type: int  
Name: ItemType, Type: varchar(10)  
Name: MiscellaneousChargeID, Type: int  
Name: MiscellaneousCharge, Type: varchar(10)  
Name: MiscellaneousChargeDescription, Type: varchar(50)  
Name: ItemNumber, Type: varchar(50)  
Name: ItemDescription, Type: varchar(50)  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: PartsOrderActionTypeID, Type: int  
Name: PartsOrderActionType, Type: varchar(50)  
Name: IsRepairOrder, Type: bit  
Name: IsMiscCharge, Type: bit  
Name: IsCore, Type: bit  
Name: IsMark, Type: bit  
Name: CustomerPurchaseOrder, Type: varchar(30)  
Name: IsQCInvoiceNumber, Type: int  
Name: Department, Type: varchar(10)  
Name: Division, Type: varchar(10)


---



### FuelInvoiceSummary 

Key: FuelInvoiceSummary,  
Type: View,  
Command: vwIN_SSR_FuelInvoiceSummary,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: FuelInvoiceID, Type: int  
Name: Division, Type: varchar(10)  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: DepartmentID, Type: int  
Name: Department, Type: varchar(10)  
Name: BillingCustomerID, Type: int  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: PONumber, Type: varchar(30)  
Name: InvoiceNumber, Type: varchar(50)  
Name: AccountingPeriodID, Type: int  
Name: PostingPeriod, Type: varchar(33)  
Name: InvoiceDate, Type: datetime  
Name: TotalFuel, Type: decimal  
Name: TotalMisc, Type: decimal  
Name: TotalTax, Type: decimal  
Name: TotalCost, Type: decimal  
Name: TotalMiscCost, Type: decimal  
Name: TotalFuelCost, Type: decimal  
Name: InvoiceSubTotal, Type: decimal  
Name: InvoiceTotal, Type: decimal  
Name: DiscountAmount, Type: decimal  
Name: PaymentMethod, Type: varchar(35)  
Name: PaymentTerms, Type: varchar(50)  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: FuelTicketCount, Type: int  
Name: DueDate, Type: datetime


---



### FuelTicket 

Key: FuelTicket,  
Type: View,  
Command: vwIN_SSR_FuelTicket,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: FuelTicketID, Type: int  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: DepartmentID, Type: int  
Name: Department, Type: varchar(10)  
Name: BillingCustomerID, Type: int  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: BillingCustomerAddressID, Type: int  
Name: TicketNumber, Type: int  
Name: TicketDate, Type: datetime  
Name: FuelTicketStatus, Type: varchar(8)  
Name: TaxCodeID, Type: int  
Name: TaxStatus, Type: varchar(50)  
Name: TaxBodyID, Type: int  
Name: TaxBody, Type: varchar(50)  
Name: PurchaseOrder, Type: varchar(30)  
Name: UserDefinedPaymentMethodID, Type: int  
Name: PaymentMethod, Type: varchar(50)  
Name: TicketTotal, Type: decimal  
Name: TaxTotal, Type: decimal  
Name: UnitInventoryID, Type: int  
Name: UnitID, Type: int  
Name: UnitNumber, Type: varchar(20)  
Name: MeterReadingID, Type: int  
Name: FuelTicketInvoiceID, Type: int  
Name: InvoiceNumber, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: Source, Type: varchar(50)  
Name: FuelInvoiceID, Type: int  
Name: ClosedFuelTicketID, Type: int  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: FuelCharges, Type: decimal  
Name: MiscCharges, Type: decimal  
Name: MeterReading, Type: decimal  
Name: ContractNumber, Type: int  
Name: LeaseContractID, Type: int  
Name: IsVoided, Type: int  
Name: IsLRInvoice, Type: int


---



### FuelTicketDetail 

Key: FuelTicketDetail,  
Type: View,  
Command: vwIN_SSR_FuelTicketDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: TicketNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: FuelTicketDetailsID, Type: int  
Name: FuelTicketID, Type: int  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: TicketNumber, Type: int  
Name: TicketDate, Type: datetime  
Name: FuelID, Type: int  
Name: Tank, Type: varchar(10)  
Name: PumpID, Type: int  
Name: Pump, Type: varchar(15)  
Name: MiscellaneousChargeID, Type: int  
Name: Item, Type: varchar(50)  
Name: Description, Type: varchar(50)  
Name: AverageCost, Type: decimal  
Name: Cost, Type: decimal  
Name: MarketRate, Type: decimal  
Name: Price, Type: decimal  
Name: Quantity, Type: decimal  
Name: ExtendedPrice, Type: decimal  
Name: FuelTicketDetailsInvoiceID, Type: int  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: FuelTicketInvoiceID, Type: int  
Name: ItemType, Type: varchar(4)  
Name: DepartmentID, Type: int  
Name: Department, Type: varchar(10)  
Name: Division, Type: varchar(10)  
Name: ExtendedAverageCost, Type: decimal  
Name: ExtendedCost, Type: decimal  
Name: ExtendedMarketRate, Type: decimal  
Name: InvoiceDate, Type: datetime  
Name: InvoiceNumber, Type: varchar(50)  
Name: OrderStatus, Type: varchar(8)  
Name: StockNumber, Type: varchar(20)  
Name: UnitNumber, Type: varchar(20)  
Name: IsVoided, Type: int  
Name: IsLRInvoice, Type: int  
Name: FuelInvoiceID, Type: int  
Name: UnitInventoryID, Type: int


---



### KitAssemblyDetail

Key: KitAssemblyDetail,  
Type: View,  
Command: vwIN_SSR_KitAssemblyDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: Branch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: PartNumber, Type: varchar(50)  
Name: PartsInventoryID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: Supplier, Type: varchar(20)  
Name: SupplierID, Type: int  
Name: SupplierName, Type: varchar(100)  
Name: PartDescription, Type: varchar(50)  
Name: CorePartNumber, Type: int  
Name: CoreSupplier, Type: int  
Name: CoreDescription, Type: int  
Name: KitAndAssemblyType, Type: varchar(10)  
Name: UpdateDetailSalesHistoryAsKitIsBuilt, Type: bit  
Name: PrintDetailOnInvoice, Type: bit  
Name: PrintRelatedCoreDetailOnInvoice, Type: bit  
Name: BinLocation, Type: varchar(20)  
Name: StockStatus, Type: varchar(50)  
Name: QuantityAvailable, Type: int  
Name: ReplacementCost, Type: decimal  
Name: AverageCost, Type: decimal  
Name: InherentCoreReplacementCost, Type: int  
Name: InherentCoreAverageCost, Type: int  
Name: DetailPartNumber, Type: varchar(50)  
Name: DetailPartsInventoryID, Type: int  
Name: DetailPartsInventoryDetailID, Type: int  
Name: DetailSupplier, Type: varchar(20)  
Name: DetailSupplierID, Type: int  
Name: DetailPartDescription, Type: varchar(50)  
Name: DetailQuantityRequired, Type: int  
Name: DetailType, Type: varchar(20)  
Name: DetailBinLocation, Type: varchar(20)  
Name: DetailStockStatus, Type: varchar(50)  
Name: DetailQuantityAvailable, Type: int  
Name: DetailReplacementCost, Type: decimal  
Name: DetailAverageCost, Type: decimal


---



### LostSales 

Key: LostSales,  
Type: View,  
Command: vwIN_SSR_LostSales,  
HasReturn: false,  
ReturnType:  
DefaultSort: CustomerNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: LostSaleID, Type: int  
Name: Branch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: PartNumber, Type: varchar(50)  
Name: PartsInventoryDetailID, Type: int  
Name: Supplier, Type: varchar(20)  
Name: StockStatus, Type: varchar(50)  
Name: Description, Type: varchar(50)  
Name: Quantity, Type: int  
Name: LostSaleReason, Type: varchar(50)  
Name: LostSaleDate, Type: datetime  
Name: ReplacementCost, Type: decimal  
Name: User, Type: varchar(20)  
Name: Application, Type: varchar(75)  
Name: LostSaleComment, Type: varchar(50)  
Name: CustomerNumber, Type: varchar(10)  
Name: CustomerID, Type: int  
Name: CustomerName, Type: varchar(100)  
Name: LostSaleMonth, Type: int  
Name: LostSaleYear, Type: int  
Name: IsCurrentYear, Type: bit  
Name: AddDate, Type: datetime  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)


---



### PartsBackOrders 

Key: PartsBackOrders,  
Type: View,  
Command: vwIN_SSR_PartsBackOrders,  
HasReturn: false,  
ReturnType:  
DefaultSort: RepairOrderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: CustomerBackorderID, Type: int  
Name: BranchID, Type: int  
Name: BranchCode, Type: varchar(10)  
Name: PartsInventoryID, Type: int  
Name: Quantity, Type: int  
Name: NoCharge, Type: bit  
Name: Price, Type: decimal  
Name: OriginalPrice, Type: decimal  
Name: CorePrice, Type: decimal  
Name: OriginalCorePrice, Type: decimal  
Name: BackorderPriorityID, Type: int  
Name: ShipComplete, Type: bit  
Name: RepairOrderID, Type: int  
Name: PartsSalesOrderID, Type: int  
Name: SalespersonID, Type: int  
Name: BackorderDate, Type: datetime  
Name: RepairOrderTaskID, Type: int  
Name: PartPurchaseOrderHeaderID, Type: int  
Name: AddUserID, Type: int  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: LastUpdate, Type: datetime  
Name: AddDateTimeZone, Type: decimal  
Name: LastUpdateTimeZone, Type: decimal  
Name: CustomerID, Type: int  
Name: CustomerKey, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: PartNumber, Type: varchar(50)  
Name: Description, Type: varchar(50)  
Name: SupplierID, Type: int  
Name: SupplierCode, Type: varchar(20)  
Name: BackorderPriority, Type: varchar(50)  
Name: DepartmentID, Type: int  
Name: Department, Type: varchar(10)  
Name: OrderingDepartment, Type: varchar(7)  
Name: Status, Type: varchar(15)  
Name: CorePartsInventoryID, Type: int  
Name: CorePartNumber, Type: varchar(50)  
Name: SalesOrderNumber, Type: int  
Name: RepairOrderNumber, Type: int  
Name: Salesperson, Type: varchar(20)  
Name: TaskNumber, Type: int  
Name: Street1, Type: varchar(100)  
Name: Street2, Type: varchar(100)  
Name: City, Type: varchar(100)  
Name: RegionID, Type: int  
Name: Region, Type: varchar(6)  
Name: PostalCode, Type: varchar(15)  
Name: PONumber, Type: varchar(10)  
Name: PurchaseOrderStatus, Type: varchar(20)  
Name: DetailDeliveryDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: PartTypeID, Type: int  
Name: PartTypeDescription, Type: varchar(20)  
Name: PartPurchaseOrderDetailID, Type: int  
Name: QuantityAvailable, Type: int  
Name: CoreDescription, Type: varchar(50)  
Name: CoreSupplierID, Type: int  
Name: CoreSupplierCode, Type: varchar(20)  
Name: PartsInventoryDetailID, Type: int  
Name: BackOrderPriorityForStockOrdersID, Type: int  
Name: FromBranchID, Type: int  
Name: FromBranch, Type: varchar(10)  
Name: APVendorID, Type: int  
Name: APVendor, Type: varchar(10)  
Name: PartsOrderActionTypeID, Type: int  
Name: InsideSalespersonID, Type: int  
Name: InsideSalesperson, Type: varchar(20)  
Name: CustomerPONumber, Type: varchar(30)  
Name: DirectShip, Type: bit  
Name: PODetail_PartPurchaseOrderStatusID, Type: int  
Name: APVendorName, Type: varchar(100)  
Name: BackorderAging, Type: varchar(5)  
Name: DaysOld, Type: int


---



### PartsCommitted 

Key: PartsCommitted,  
Type: View,  
Command: vwIN_SSR_PartsCommitted,  
HasReturn: false,  
ReturnType:  
DefaultSort: OrderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartNumber, Type: varchar(50)  
Name: CustomerID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: SupplierID, Type: int  
Name: SupplierCode, Type: varchar(20)  
Name: Description, Type: varchar(50)  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: CommittedDate, Type: datetime  
Name: Quantity, Type: int  
Name: OrderNumber, Type: varchar(50)  
Name: OrderID, Type: int  
Name: Module, Type: varchar(7)  
Name: RequestingBranch, Type: varchar(10)  
Name: SellingPrice, Type: decimal  
Name: SellingCost, Type: decimal  
Name: ExtendedReplacementCost, Type: decimal  
Name: AverageCost, Type: decimal  
Name: ExtendedAverageCost, Type: decimal  
Name: ExtendedSellingPrice, Type: decimal  
Name: PartType, Type: varchar(50)  
Name: AssemblyPartNumber, Type: varchar(50)  
Name: IsAssemblyDetail, Type: bit


---



### PartsMessages 

Key: PartsMessages,  
Type: View,  
Command: vwIN_SSR_PartsMessages,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartMessageID, Type: int  
Name: PartMessageTypeID, Type: int  
Name: MessageType, Type: varchar(30)  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: PartsInventoryID, Type: int  
Name: SupplierID, Type: int  
Name: SupplierCode, Type: varchar(20)  
Name: PartTypeID, Type: int  
Name: PartType, Type: varchar(20)  
Name: MessageDescription, Type: varchar(8000)  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: PartNumber, Type: varchar(50)  
Name: PartsInventoryDetailID, Type: int  
Name: PartDescription, Type: varchar(50)


---



### PartsOrder 

Key: PartsOrder,  
Type: View,  
Command: vwIN_SSR_PartsOrder,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartsOrderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsSalesOrderID, Type: int  
Name: BranchID, Type: int  
Name: DepartmentID, Type: int  
Name: CustomerID, Type: int  
Name: BillingCustomerID, Type: int  
Name: TaxCodeID, Type: int  
Name: TaxBodyID, Type: int  
Name: LocalPurchaseOrderID, Type: int  
Name: PartsSalesOrderInvoiceID, Type: int  
Name: PickupDeliveryMethodID, Type: int  
Name: SalesOrderStatusID, Type: int  
Name: JoinID, Type: varchar(50)  
Name: CanadianTaxID, Type: varchar(15)  
Name: QuebecTaxID, Type: varchar(16)  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: Department, Type: varchar(10)  
Name: PartsOrderNumber, Type: int  
Name: OrderStatus, Type: varchar(50)  
Name: CreationDate, Type: datetime  
Name: CustomerNumber, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: CustomerPO, Type: varchar(30)  
Name: PickupDeliveryMethod, Type: varchar(100)  
Name: DeliveryDate, Type: datetime  
Name: TrackingNumber, Type: varchar(250)  
Name: InvoiceDate, Type: datetime  
Name: InvoiceNumber, Type: varchar(50)  
Name: LastUpdate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: UpdateUser, Type: varchar(20)  
Name: InvoiceUser, Type: varchar(20)  
Name: BillingCustomerAccountStatus, Type: varchar(50)  
Name: BillingContactName, Type: varchar(201)  
Name: BillingHomePhone, Type: varchar(30)  
Name: BillingWorkPhone, Type: varchar(30)  
Name: BillingCustomerNumber, Type: varchar(10)  
Name: BillingCompanyName, Type: varchar(100)  
Name: TaxCode, Type: varchar(50)  
Name: TaxBody, Type: varchar(50)  
Name: IsLocal, Type: bit  
Name: LPO, Type: int  
Name: OutsidePartsSalesperson, Type: varchar(201)  
Name: PartsAccounting, Type: varchar(50)  
Name: Source, Type: varchar(20)  
Name: ContactName, Type: varchar(201)  
Name: ContactHomePhone, Type: varchar(30)  
Name: ContactWorkPhone, Type: varchar(30)  
Name: ShipToCustomerName, Type: varchar(100)  
Name: ShipToAddress1, Type: varchar(100)  
Name: ShipToAddress2, Type: varchar(100)  
Name: ShipToCity, Type: varchar(100)  
Name: ShipToRegion, Type: varchar(6)  
Name: ShipToPostalCode, Type: varchar(15)  
Name: ShipToOfficePhone, Type: varchar(30)  
Name: ShipToFax, Type: varchar(30)  
Name: ShipToShopPhone, Type: varchar(30)  
Name: ShipToEmail, Type: varchar(100)  
Name: AverageCost, Type: decimal  
Name: ReplacementCost, Type: decimal  
Name: OrderSubtotal, Type: decimal  
Name: OrderTotal, Type: decimal  
Name: SalesTaxTotal, Type: decimal  
Name: AverageCostGrossProfit, Type: decimal  
Name: ReplacementCostGrossProfit, Type: decimal  
Name: AverageCostGrossProfitMargin, Type: decimal  
Name: ReplacementCostGrossProfitMargin, Type: decimal  
Name: SalesTerritory, Type: varchar(50)  
Name: CustomerAccountStatus, Type: varchar(50)  
Name: ItemsReadyforPickup, Type: int  
Name: UpdateStatus, Type: varchar(20)  
Name: IsVoided, Type: bit  
Name: PaymentMethod, Type: varchar(50)  
Name: UserDefinedPaymentMethodID, Type: int  
Name: StaticPaymentMethodID, Type: int  
Name: Territory, Type: varchar(50)


---



### PartsOrderDetail 

Key: PartsOrderDetail,  
Type: View,  
Command: vwIN_SSR_PartsOrderDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartsOrderNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsSalesOrderID, Type: int  
Name: PartsSalesOrderPartsID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: PartsSalesOrderInvoiceID, Type: int  
Name: Division, Type: varchar(10)  
Name: Branch, Type: varchar(10)  
Name: BranchID, Type: int  
Name: Department, Type: varchar(10)  
Name: Local, Type: bit  
Name: PartNumber, Type: varchar(50)  
Name: PartType, Type: varchar(4)  
Name: AverageCost, Type: decimal  
Name: ExtendedAverageCost, Type: decimal  
Name: ReplacementCost, Type: decimal  
Name: ExtendedReplacementCost, Type: decimal  
Name: Price, Type: decimal  
Name: CalculatedPrice, Type: decimal  
Name: OverridePrice, Type: decimal  
Name: ExtendedPrice, Type: decimal  
Name: Quantity, Type: int  
Name: AddDate, Type: datetime  
Name: PartsOrderNumber, Type: int  
Name: OrderStatus, Type: varchar(50)  
Name: PartsActionType, Type: varchar(50)  
Name: BackOrderPriority, Type: varchar(50)  
Name: CreationDate, Type: datetime  
Name: SellingCost, Type: decimal  
Name: ExtendedSellingCost, Type: decimal  
Name: MPOReference, Type: varchar(50)  
Name: PartsAccounting, Type: varchar(50)  
Name: DetailPartMessage, Type: varchar(7500)  
Name: IsNoChargeTransaction, Type: bit  
Name: DeliveryDate, Type: datetime  
Name: PickupDeliveryMethod, Type: varchar(100)  
Name: PriceOverrideReason, Type: varchar(30)  
Name: ItemType, Type: varchar(4)  
Name: IsBackorder, Type: bit  
Name: ReadyForPickup, Type: bit  
Name: UpdateStatus, Type: varchar(1)  
Name: IsPartialFill, Type: bit  
Name: InvoiceNumber, Type: varchar(50)  
Name: InvoiceDate, Type: datetime  
Name: OEMPrice, Type: decimal  
Name: OEMRebateAmount, Type: decimal  
Name: InsidePartsSalesperson, Type: varchar(20)  
Name: OutsidePartsSalesperson, Type: varchar(20)  
Name: ItemDescription, Type: varchar(50)  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: Supplier, Type: varchar(20)  
Name: ReturnReason, Type: varchar(50)  
Name: JoinID, Type: varchar(50)  
Name: UnitOfMeasure, Type: varchar(50)  
Name: BinLocation, Type: varchar(20)  
Name: PartsInventoryKitTypeID, Type: int  
Name: IsPOSAssembly, Type: bit


---



### PartsPO 

Key: PartsPO,  
Type: View,  
Command: vwIN_SSR_PartsPO,  
HasReturn: false,  
ReturnType:  
DefaultSort: PONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartPurchaseOrderHeaderID, Type: int  
Name: SupplierID, Type: int  
Name: BranchID, Type: int  
Name: FromBranchID, Type: int  
Name: APVendorID, Type: int  
Name: PartPurchaseOrderStatusID, Type: int  
Name: OrderedByUserID, Type: int  
Name: AddUserID, Type: int  
Name: UpdateUserID, Type: int  
Name: QL_OrderGroupID, Type: int  
Name: PurchaseOrderSourceID, Type: varchar(30)  
Name: Branch, Type: varchar(10)  
Name: APVendor, Type: varchar(10)  
Name: VendorCompanyName, Type: varchar(100)  
Name: PONumber, Type: varchar(10)  
Name: Status, Type: varchar(20)  
Name: OrderedByUser, Type: varchar(20)  
Name: FillingBranch, Type: varchar(10)  
Name: SupplierCode, Type: varchar(20)  
Name: Name, Type: varchar(100)  
Name: PurchaseOrderDate, Type: datetime  
Name: BOPriority, Type: varchar(50)  
Name: OEMReferenceNumber, Type: varchar(20)  
Name: PurchaseOrderSource, Type: varchar(30)  
Name: InterBranchStockOrder, Type: bit  
Name: ReturnPurchaseOrder, Type: bit  
Name: DirectShip, Type: bit  
Name: PartsTotal, Type: decimal  
Name: CoreChargeTotal, Type: decimal  
Name: CoreReturnTotal, Type: decimal  
Name: Total, Type: decimal  
Name: TotalPieces, Type: int  
Name: TotalWeight, Type: decimal  
Name: CompanyName, Type: varchar(100)  
Name: ShipToAddress1, Type: varchar(100)  
Name: ShipToAddress2, Type: varchar(100)  
Name: ShipToCity, Type: varchar(100)  
Name: ShipToRegion, Type: varchar(6)  
Name: ShipToPostalCode, Type: varchar(15)  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: IsAllSupplier, Type: bit


---



### PartsPODetail 

Key: PartsPODetail,  
Type: View,  
Command: vwIN_SSR_PartsPODetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: PONumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartPurchaseOrderDetailID, Type: int  
Name: PartPurchaseOrderHeaderID, Type: int  
Name: SupplierCode, Type: varchar(20)  
Name: SupplierName, Type: varchar(100)  
Name: SupplierID, Type: int  
Name: PartNumber, Type: varchar(50)  
Name: PartDescription, Type: varchar(50)  
Name: PartsInventoryDetailID, Type: int  
Name: Quantity, Type: int  
Name: Cost, Type: decimal  
Name: CoreCost, Type: decimal  
Name: AverageCost, Type: decimal  
Name: InherentAverageCoreCost, Type: decimal  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: CorePartID, Type: int  
Name: CorePartNumber, Type: varchar(50)  
Name: CorePartDescription, Type: varchar(50)  
Name: PONumber, Type: varchar(10)  
Name: StockStatus, Type: varchar(50)  
Name: ExtendedCost, Type: decimal  
Name: ExtendedCoreCost, Type: decimal  
Name: ExtendedAverageCost, Type: decimal  
Name: ExtendedInherentAverageCoreCost, Type: decimal  
Name: BinLocation, Type: varchar(20)  
Name: UnitOfMeasure, Type: varchar(50)  
Name: Message, Type: varchar(250)  
Name: ImportCost, Type: decimal  
Name: CoreImportCost, Type: decimal  
Name: DetailDeliveryDate, Type: datetime  
Name: Status, Type: varchar(20)  
Name: Branch, Type: varchar(10)  
Name: Division, Type: varchar(10)  
Name: FillingBranch, Type: varchar(10)  
Name: InterBranchStockOrder, Type: bit  
Name: InterBranchBackorder, Type: int


---



### PartsTransactions 

Key: PartsTransactions,  
Type: View,  
Command: vwIN_SSR_PartsTransactions,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartBranch, Type: varchar(10)  
Name: PartsInventoryID, Type: int  
Name: PartsInventoryTransactionID, Type: int  
Name: BranchID, Type: int  
Name: Supplier, Type: varchar(20)  
Name: SupplierID, Type: int  
Name: SupplierName, Type: varchar(100)  
Name: PartNumber, Type: varchar(50)  
Name: PartsInventoryDetailID, Type: int  
Name: PartDescription, Type: varchar(50)  
Name: DateTime, Type: datetime  
Name: Username, Type: varchar(20)  
Name: SourceDocument, Type: varchar(100)  
Name: ChangeAction, Type: varchar(50)  
Name: ChangedField, Type: varchar(50)  
Name: NewQty, Type: int  
Name: AverageCost, Type: decimal  
Name: ReplacementCost, Type: decimal  
Name: PartType, Type: varchar(20)  
Name: QuantityAdjustmentReason, Type: varchar(50)  
Name: OldValue, Type: varchar(100)  
Name: NewValue, Type: varchar(100)  
Name: Difference, Type: decimal  
Name: QuantityAvailable, Type: int  
Name: InherentReplacementCost, Type: decimal  
Name: InherentAverageCost, Type: decimal  
Name: Application, Type: varchar(75)  
Name: Price1, Type: decimal  
Name: Price2, Type: decimal  
Name: Price3, Type: decimal  
Name: Price4, Type: decimal  
Name: Price5, Type: decimal  
Name: Price6, Type: decimal  
Name: Price7, Type: decimal  
Name: PreviousPrice1, Type: decimal  
Name: PreviousPrice2, Type: decimal  
Name: PreviousPrice3, Type: decimal  
Name: PreviousPrice4, Type: decimal  
Name: PreviousPrice5, Type: decimal  
Name: PreviousPrice6, Type: decimal  
Name: PreviousPrice7, Type: decimal  
Name: ListPrice, Type: decimal  
Name: PreviousListPrice, Type: decimal  
Name: PreviousAverageCost, Type: decimal  
Name: PreviousInherentAverageCost, Type: decimal  
Name: PreviousReplacementCost, Type: decimal  
Name: PreviousInherentReplacementCost, Type: decimal  
Name: PreviousQuantityAvailable, Type: int


---



### PartsVendorRebates 

Key: PartsVendorRebates,  
Type: View,  
Command: vwIN_SSR_PartsVendorRebates,  
HasReturn: false,  
ReturnType:  
DefaultSort: InvoiceNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: VendorRebateHistoricalID, Type: int  
Name: StockClass, Type: varchar(10)  
Name: Code1, Type: varchar(10)  
Name: Code2, Type: varchar(10)  
Name: Code3, Type: varchar(10)  
Name: Code4, Type: varchar(10)  
Name: Code5, Type: varchar(10)  
Name: ExpirationDate, Type: datetime  
Name: Multiplier, Type: decimal  
Name: UseRebatedCostAtTimeOfSale, Type: bit  
Name: CalculateCommissionsBasedOnRebatedCost, Type: bit  
Name: RecordNotes, Type: varchar(100)  
Name: ValuePriceLevel, Type: decimal  
Name: VendorPrice, Type: decimal  
Name: RebateAmount, Type: decimal  
Name: ExtendedRebateAmount, Type: decimal  
Name: AddUser, Type: varchar(20)  
Name: InvoiceDate, Type: datetime  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime  
Name: Customer, Type: varchar(10)  
Name: CustomerName, Type: varchar(100)  
Name: InvoiceNumber, Type: varchar(50)  
Name: Branch, Type: varchar(100)  
Name: PartDescription, Type: varchar(50)  
Name: Quantity, Type: int  
Name: Vendor, Type: varchar(100)  
Name: InsideSalesperson, Type: varchar(100)  
Name: OutsideSalesperson, Type: varchar(100)  
Name: SellingPrice, Type: decimal  
Name: PartNumber, Type: varchar(50)  
Name: Supplier, Type: varchar(100)  
Name: CustomerPricingType, Type: varchar(50)  
Name: PriceLevel, Type: varchar(50)  
Name: PriceFileSource, Type: varchar(50)  
Name: AverageCost, Type: decimal  
Name: ReplacementCost, Type: decimal  
Name: VendorPriceDescription, Type: varchar(50)


---



### Supplier 

Key: Supplier,  
Type: View,  
Command: vwIN_SSR_Supplier,  
HasReturn: false,  
ReturnType:  
DefaultSort: NAME,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: SupplierID, Type: int  
Name: SupplierCode, Type: varchar(20)  
Name: NAME, Type: varchar(100)  
Name: PriceGroup, Type: varchar(50)  
Name: QL_DefaultSellingUnitOfMeasureID, Type: int  
Name: UnitOfMeasure, Type: varchar(50)  
Name: DefaultProductClassID, Type: int  
Name: Inactive, Type: bit  
Name: BranchID, Type: int  
Name: APVendor, Type: varchar(10)  
Name: CompanyName, Type: varchar(100)  
Name: APVendorID, Type: int  
Name: StockClass, Type: varchar(10)  
Name: Code1, Type: varchar(10)  
Name: Code2, Type: varchar(10)  
Name: Code3, Type: varchar(10)  
Name: Code4, Type: varchar(10)  
Name: Code5, Type: varchar(10)  
Name: AlternateSupplierID, Type: int  
Name: OrderGroupID, Type: int  
Name: UpdateFromPriceFile, Type: bit  
Name: TrackAvailableQuantity, Type: bit  
Name: ReplacementCostMultiplier, Type: decimal  
Name: Price1Multiplier, Type: decimal  
Name: Price2Multiplier, Type: decimal  
Name: Price3Multiplier, Type: decimal  
Name: Price4Multiplier, Type: decimal  
Name: Price5Multiplier, Type: decimal  
Name: Price6Multiplier, Type: decimal  
Name: Price7Multiplier, Type: decimal  
Name: ListMultiplier, Type: decimal  
Name: PurchaseMethodID, Type: int  
Name: SafetyStockPercent, Type: int  
Name: LastOrderDate, Type: datetime  
Name: LeadTime, Type: int  
Name: OrderFrequency, Type: int  
Name: DaysOfStock, Type: int  
Name: BuyTime, Type: int  
Name: MinimumOrderDollar, Type: int  
Name: MaximumOrderWeight, Type: int  
Name: SuggestedOrderMonths, Type: int  
Name: CoreRightToReturnDaysCustomer, Type: int  
Name: CoreRightToReturnDaysSupplier, Type: int  
Name: AddressID, Type: int  
Name: ContactID, Type: int  
Name: DefaultPriceFileSourceID, Type: int  
Name: OEMBreakdown, Type: bit  
Name: AccountingGroupID, Type: int  
Name: AccountingGroup, Type: varchar(10)  
Name: IsOEMBreakdownPrinted, Type: bit  
Name: BarCodeMultiplierID, Type: int  
Name: CurrencyExchangeCodeID, Type: int  
Name: CurrencyCode, Type: varchar(10)  
Name: CurrencyExchangeDutyCodeID, Type: int  
Name: DutyCode, Type: varchar(50)  
Name: CurrencyExchangeBrokerID, Type: int  
Name: CurrencyExchangeBroker, Type: varchar(50)  
Name: ImportFreightMultiplier, Type: decimal  
Name: ManufacturerCode, Type: varchar(10)  
Name: Seasonal, Type: bit  
Name: AlternateSupplier, Type: varchar(20)  
Name: PriceFileSource, Type: varchar(20)  
Name: ProductClass, Type: varchar(50)  
Name: PurchaseMethod, Type: varchar(20)  
Name: OrderGroup, Type: varchar(50)  
Name: BarCodeMultiplier, Type: varchar(25)  
Name: Salutation, Type: varchar(50)  
Name: FirstName, Type: varchar(100)  
Name: LastName, Type: varchar(100)  
Name: Title, Type: varchar(50)  
Name: OfficePhone, Type: varchar(30)  
Name: ShopPhone, Type: varchar(30)  
Name: CellPhone, Type: varchar(30)  
Name: Fax, Type: varchar(30)  
Name: E-MailAddress, Type: varchar(100)  
Name: WebAddress, Type: varchar(100)  
Name: Address1, Type: varchar(100)  
Name: Address2, Type: varchar(100)  
Name: City, Type: varchar(100)  
Name: Region, Type: varchar(6)  
Name: PostalCode, Type: varchar(15)  
Name: Country, Type: varchar(35)  
Name: County, Type: varchar(35)  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: MinimumReturnDollar, Type: int  
Name: MinimumReturnWeight, Type: int  
Name: CharacteristicType, Type: varchar(20)


---



### SupplierCoreRTR 

Key: SupplierCoreRTR,  
Type: View,  
Command: vwIN_SSR_SupplierCoreRTR,  
HasReturn: false,  
ReturnType:  
DefaultSort: APVendor,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: SupplierCoreRighttoReturnID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: APVendorID, Type: int  
Name: BranchID, Type: int  
Name: BranchCode, Type: varchar(10)  
Name: APVendor, Type: varchar(10)  
Name: APVendorName, Type: varchar(100)  
Name: PartsInventoryID, Type: int  
Name: PartNumber, Type: varchar(50)  
Name: SupplierCode, Type: varchar(20)  
Name: SupplierID, Type: int  
Name: Description, Type: varchar(50)  
Name: QuantityAvailable, Type: int  
Name: ReceivedDate, Type: datetime  
Name: PostingReference, Type: varchar(50)  
Name: ReceivedCost, Type: decimal  
Name: ExpirationDate, Type: datetime  
Name: QuantityReceived, Type: int  
Name: QuantityReturned, Type: int  
Name: QuantityRemaining, Type: int  
Name: CoreRightToReturnDaysSupplier, Type: int  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDateTime, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdateTime, Type: datetime  
Name: CoreSupplier, Type: varchar(20)  
Name: TotalOwedForPartNumber, Type: int  
Name: TotalOwedToAPVendorForPartNumber, Type: int

## Parts Inventory



---



### PartsInventory 

Key: PartsInventory,  
Type: View,  
Command: vwIN_SSR_PartsInventory,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsInventoryDetailID, Type: int  
Name: PartNumber, Type: varchar(50)  
Name: PartType, Type: varchar(20)  
Name: SupplierCode, Type: varchar(20)  
Name: SupplierID, Type: int  
Name: Description, Type: varchar(50)  
Name: CorePartsInventoryID, Type: int  
Name: PartsInventoryID, Type: int  
Name: BranchCode, Type: varchar(10)  
Name: BranchID, Type: int  
Name: QuantityAvailable, Type: int  
Name: QuantityCommitted, Type: int  
Name: QuantityOnOrder, Type: int  
Name: QuantityOnBackOrder, Type: int  
Name: AverageCost, Type: decimal  
Name: ReplacementCost, Type: decimal  
Name: Price1, Type: decimal  
Name: Price2, Type: decimal  
Name: Price3, Type: decimal  
Name: Price4, Type: decimal  
Name: Price5, Type: decimal  
Name: Price6, Type: decimal  
Name: Price7, Type: decimal  
Name: ListPrice, Type: decimal  
Name: CorePartsInventoryDetailID, Type: int  
Name: InherentCoreAverageCost, Type: decimal  
Name: BinLocation, Type: varchar(20)  
Name: Inactive, Type: bit  
Name: StockStatusID, Type: int  
Name: BarCode, Type: varchar(50)  
Name: AlternateSupplierID, Type: int  
Name: SellPackage, Type: int  
Name: IsInventory, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: AlternateBin, Type: nvarchar(max)  
Name: CharacteristicType, Type: varchar(20)


---



### PartsInventoryExtended 

Key: PartsInventoryExtended,  
Type: View,  
Command: vwIN_SSR_PartsInventoryExtended,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsInventoryDetailID, Type: int  
Name: PartNumber, Type: varchar(50)  
Name: SupplierCode, Type: varchar(20)  
Name: SupplierID, Type: int  
Name: Description, Type: varchar(50)  
Name: PartType, Type: varchar(20)  
Name: CorePartsInventoryID, Type: int  
Name: PartsInventoryID, Type: int  
Name: BranchCode, Type: varchar(10)  
Name: BranchID, Type: int  
Name: QuantityAvailable, Type: int  
Name: AverageCost, Type: decimal  
Name: CurrentMonthUsage, Type: int  
Name: CurrentMonthPicks, Type: int  
Name: 13MonthSales, Type: int  
Name: 13MonthManualSales, Type: int  
Name: 13MonthTotalSales, Type: int  
Name: 13MonthPicks, Type: int  
Name: 13MonthManualPicks, Type: int  
Name: 13MonthTotalPicks, Type: int  
Name: 13MonthTotalLostSales, Type: int  
Name: AddUserID, Type: int  
Name: UpdateUserID, Type: int  
Name: CorePartsInventoryDetailID, Type: int  
Name: InherentCoreAverageCost, Type: decimal  
Name: BinLocation, Type: varchar(20)  
Name: LastReceivedDate, Type: datetime  
Name: LastAveragingQuantity, Type: int  
Name: Inactive, Type: bit  
Name: LastSoldDate, Type: datetime  
Name: LastCountDate, Type: datetime  
Name: StockStatusID, Type: int  
Name: BarCode, Type: varchar(50)  
Name: StockClass, Type: varchar(10)  
Name: Code1, Type: varchar(10)  
Name: Code2, Type: varchar(10)  
Name: Code3, Type: varchar(10)  
Name: Code4, Type: varchar(10)  
Name: Code5, Type: varchar(10)  
Name: UpdateFromPriceFile, Type: bit  
Name: TrackAvailabilityQuantity, Type: bit  
Name: AlternateSupplierID, Type: int  
Name: InventoryClass, Type: varchar(10)  
Name: VelocityCode, Type: varchar(10)  
Name: ReturnCode, Type: varchar(10)  
Name: QL_PriceGroupID, Type: int  
Name: PriceGroup, Type: varchar(50)  
Name: SellPackage, Type: int  
Name: PriceFileFactor, Type: int  
Name: Price1, Type: decimal  
Name: Price2, Type: decimal  
Name: Price3, Type: decimal  
Name: Price4, Type: decimal  
Name: Price5, Type: decimal  
Name: Price6, Type: decimal  
Name: Price7, Type: decimal  
Name: ListPrice, Type: decimal  
Name: PurchaseMethodID, Type: int  
Name: SafetyStockPercent, Type: int  
Name: JobQuantity, Type: int  
Name: Seasonal, Type: bit  
Name: OrderPoint, Type: int  
Name: FreezeDate, Type: datetime  
Name: MinimumQuantity, Type: int  
Name: MaximumQuantity, Type: int  
Name: LeadTime, Type: int  
Name: OrderFrequency, Type: int  
Name: DaysOfStock, Type: int  
Name: BuyTime, Type: int  
Name: AverageLeadTime, Type: int  
Name: DaysOutMTD, Type: int  
Name: BuyPackage, Type: int  
Name: PurchaseConversion, Type: int  
Name: SupplierBuyPackage, Type: int  
Name: QL_PurchaseUnitOfMeasureID, Type: int  
Name: PurchUnitofMeasure, Type: varchar(50)  
Name: DateAdded, Type: datetime  
Name: LastReplacementCostChangeDate, Type: datetime  
Name: LastPriceChangeDate, Type: datetime  
Name: LastPriceFileUpdate, Type: datetime  
Name: LastOrderedDate, Type: datetime  
Name: LastOutOfStockDateGMT, Type: datetime  
Name: LastPuchaseCost, Type: decimal  
Name: QuantityCommitted, Type: int  
Name: QuantityOnOrder, Type: int  
Name: QuantityOnBackOrder, Type: int  
Name: ReplacementCost, Type: decimal  
Name: QL_SellingUnitOfMeasureID, Type: int  
Name: SellingUnitOfMeasure, Type: varchar(50)  
Name: Weight, Type: decimal  
Name: ProductClassID, Type: int  
Name: BinLocationID, Type: int  
Name: ExcludeFromCostMatrix, Type: bit  
Name: PriceFileSourceID, Type: int  
Name: PriceFilePartNumber, Type: varchar(50)  
Name: IsPriceUpdatedDuringReceiving, Type: bit  
Name: SupersedePriceFilePartNumber, Type: varchar(50)  
Name: SerialNumber, Type: varchar(20)  
Name: EHCCodeID, Type: int  
Name: EHCCode, Type: varchar(10)  
Name: AccountingGroupID, Type: int  
Name: AccountingGroup, Type: varchar(10)  
Name: ExcludeFromVelocityPricing, Type: bit  
Name: ExcludeFromPriceRounding, Type: bit  
Name: CurrencyExchangeCodeID, Type: int  
Name: CurrencyCode, Type: varchar(10)  
Name: CurrencyExchangeDutyCodeID, Type: int  
Name: DutyCode, Type: varchar(50)  
Name: CurrencyExchangeBrokerID, Type: int  
Name: CurrencyExchangeBroker, Type: varchar(50)  
Name: ImportFreightMultiplier, Type: decimal  
Name: ExcludeFromCurrencyExchange, Type: bit  
Name: ImportCost, Type: decimal  
Name: SerialStockTypeID, Type: int  
Name: IsRecommendedStockingPartFreightLiner, Type: bit  
Name: IsMissionCriticalPartFreightLiner, Type: bit  
Name: IsFleetStockingPartFreight, Type: bit  
Name: FullBinQuantity, Type: int  
Name: StockStatus, Type: varchar(50)  
Name: AlternateSupplier, Type: varchar(20)  
Name: OverrideProductClass, Type: varchar(50)  
Name: PurchaseMethod, Type: varchar(20)  
Name: BarCodeMultiplier, Type: varchar(25)  
Name: PriceFileSource, Type: varchar(20)  
Name: PriceFileSourceDescription, Type: varchar(50)  
Name: SerialStockType, Type: varchar(50)  
Name: KitType, Type: varchar(10)  
Name: CorePartNumber, Type: varchar(50)  
Name: CoreSupplier, Type: varchar(20)  
Name: CoreDescription, Type: varchar(50)  
Name: CoreReplacementCost, Type: decimal  
Name: CoreAverageCost, Type: decimal  
Name: CorePrice1, Type: decimal  
Name: CorePrice2, Type: decimal  
Name: CorePrice3, Type: decimal  
Name: CorePrice4, Type: decimal  
Name: CorePrice5, Type: decimal  
Name: CorePrice6, Type: decimal  
Name: CorePrice7, Type: decimal  
Name: CoreListPrice, Type: decimal  
Name: LifoCost, Type: decimal  
Name: LifoDate, Type: datetime  
Name: LastLifoCost, Type: decimal  
Name: LastLifoDate, Type: datetime  
Name: CountryOfOrigin, Type: varchar(50)  
Name: AlternateDescription, Type: varchar(100)  
Name: TariffNumber, Type: varchar(50)  
Name: ProductCharacteristic, Type: varchar(50)  
Name: IsPrintLabel, Type: bit  
Name: IsInventory, Type: int  
Name: AddDate, Type: datetime  
Name: AddUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: IsMDIControlled, Type: bit  
Name: AlternateBin, Type: nvarchar(max)  
Name: ExcludefromPartsASIST, Type: bit  
Name: BrandID, Type: varchar(1)  
Name: System, Type: nvarchar(256)  
Name: Assembly, Type: nvarchar(256)  
Name: Component, Type: nvarchar(256)  
Name: CharacteristicType, Type: varchar(20)


---



### PartsInventoryUsage 

Key: PartsInventoryUsage,  
Type: View,  
Command: vwIN_SSR_PartsInventoryUsage,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsInventoryDetailID, Type: int  
Name: PartsInventoryMonthlyTransactionSummaryID, Type: int  
Name: Branch, Type: varchar(10)  
Name: PartNumber, Type: varchar(50)  
Name: Supplier, Type: varchar(20)  
Name: Description, Type: varchar(50)  
Name: PartType, Type: varchar(20)  
Name: Inactive, Type: bit  
Name: BinLocation, Type: varchar(20)  
Name: BarCode, Type: varchar(50)  
Name: StockStatus, Type: varchar(50)  
Name: QuantityAvailable, Type: int  
Name: QuantityCommitted, Type: int  
Name: QuantityOnOrder, Type: int  
Name: QuantityOnBackorder, Type: int  
Name: ReplacementCost, Type: decimal  
Name: AverageCost, Type: decimal  
Name: StockClass, Type: varchar(10)  
Name: DateAdded, Type: datetime  
Name: LastSoldDate, Type: datetime  
Name: LastCountDate, Type: datetime  
Name: LastReplacementCostChangeDate, Type: datetime  
Name: LastPriceChangeDate, Type: datetime  
Name: LastPriceFileUpdate, Type: datetime  
Name: LastOrderedDate, Type: datetime  
Name: LastReceivedDate, Type: datetime  
Name: LastOutOfStockDate, Type: datetime  
Name: LIFODate, Type: datetime  
Name: Month, Type: int  
Name: Year, Type: int  
Name: Picks, Type: int  
Name: Sales, Type: int  
Name: Ignore, Type: bit  
Name: LostSales, Type: int  
Name: ManualPicks, Type: int  
Name: ManualSales, Type: int  
Name: TotalPicks, Type: int  
Name: TotalSales, Type: int  
Name: TotalLostSales, Type: int  
Name: DaysSinceLastSale, Type: int  
Name: YTDPicks, Type: int  
Name: YTDSales, Type: int  
Name: PYPicks, Type: int  
Name: PYSales, Type: int  
Name: PYTDPicks, Type: int  
Name: PYTDSales, Type: int


---



### PartsInventoryUsageTrailing12Months 

Key: PartsInventoryUsageTrailing12Months,  
Type: View,  
Command: vwIN_SSR_PartsInventoryUsageTrailing12Months,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: Branch, Type: varchar(10)  
Name: Supplier, Type: varchar(20)  
Name: PartNumber, Type: varchar(50)  
Name: PartsInventoryDetailID, Type: int  
Name: DateAdded, Type: datetime  
Name: SuggestedOrderMonths, Type: int  
Name: CurrentMonth, Type: int  
Name: CurrentYear, Type: int  
Name: CurrentMonthSales, Type: int  
Name: JanSales, Type: int  
Name: FebSales, Type: int  
Name: MarSales, Type: int  
Name: AprSales, Type: int  
Name: MaySales, Type: int  
Name: JunSales, Type: int  
Name: JulSales, Type: int  
Name: AugSales, Type: int  
Name: SepSales, Type: int  
Name: OctSales, Type: int  
Name: NovSales, Type: int  
Name: DecSales, Type: int  
Name: CurrentMonthPicks, Type: int  
Name: JanPicks, Type: int  
Name: FebPicks, Type: int  
Name: MarPicks, Type: int  
Name: AprPicks, Type: int  
Name: MayPicks, Type: int  
Name: JunPicks, Type: int  
Name: JulPicks, Type: int  
Name: AugPicks, Type: int  
Name: SepPicks, Type: int  
Name: OctPicks, Type: int  
Name: NovPicks, Type: int  
Name: DecPicks, Type: int  
Name: CurrentMonthManualSales, Type: int  
Name: JanManualSales, Type: int  
Name: FebManualSales, Type: int  
Name: MarManualSales, Type: int  
Name: AprManualSales, Type: int  
Name: MayManualSales, Type: int  
Name: JunManualSales, Type: int  
Name: JulManualSales, Type: int  
Name: AugManualSales, Type: int  
Name: SepManualSales, Type: int  
Name: OctManualSales, Type: int  
Name: NovManualSales, Type: int  
Name: DecManualSales, Type: int  
Name: CurrentMonthManualPicks, Type: int  
Name: JanManualPicks, Type: int  
Name: FebManualPicks, Type: int  
Name: MarManualPicks, Type: int  
Name: AprManualPicks, Type: int  
Name: MayManualPicks, Type: int  
Name: JunManualPicks, Type: int  
Name: JulManualPicks, Type: int  
Name: AugManualPicks, Type: int  
Name: SepManualPicks, Type: int  
Name: OctManualPicks, Type: int  
Name: NovManualPicks, Type: int  
Name: DecManualPicks, Type: int  
Name: CurrentMonthTotalSales, Type: int  
Name: JanTotalSales, Type: int  
Name: FebTotalSales, Type: int  
Name: MarTotalSales, Type: int  
Name: AprTotalSales, Type: int  
Name: MayTotalSales, Type: int  
Name: JunTotalSales, Type: int  
Name: JulTotalSales, Type: int  
Name: AugTotalSales, Type: int  
Name: SepTotalSales, Type: int  
Name: OctTotalSales, Type: int  
Name: NovTotalSales, Type: int  
Name: DecTotalSales, Type: int  
Name: CurrentMonthTotalPicks, Type: int  
Name: JanTotalPicks, Type: int  
Name: FebTotalPicks, Type: int  
Name: MarTotalPicks, Type: int  
Name: AprTotalPicks, Type: int  
Name: MayTotalPicks, Type: int  
Name: JunTotalPicks, Type: int  
Name: JulTotalPicks, Type: int  
Name: AugTotalPicks, Type: int  
Name: SepTotalPicks, Type: int  
Name: OctTotalPicks, Type: int  
Name: NovTotalPicks, Type: int  
Name: DecTotalPicks, Type: int  
Name: Trailing12MonthSales, Type: int  
Name: Trailing12MonthPicks, Type: int  
Name: Trailing12MonthManualSales, Type: int  
Name: Trailing12MonthManualPicks, Type: int  
Name: Trailing12MonthTotalSales, Type: int  
Name: Trailing12MonthTotalPicks, Type: int


---



### PartsInventoryYearlyUsage 

Key: PartsInventoryYearlyUsage,  
Type: View,  
Command: vwIN_SSR_PartsInventoryYearlyUsage,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PartsInventoryDetailID, Type: int  
Name: Branch, Type: varchar(10)  
Name: PartNumber, Type: varchar(50)  
Name: Supplier, Type: varchar(20)  
Name: Description, Type: varchar(50)  
Name: PartType, Type: varchar(20)  
Name: Inactive, Type: bit  
Name: BinLocation, Type: varchar(20)  
Name: BarCode, Type: varchar(50)  
Name: StockStatus, Type: varchar(50)  
Name: Year, Type: int  
Name: JanPicks, Type: int  
Name: FebPicks, Type: int  
Name: MarPicks, Type: int  
Name: AprPicks, Type: int  
Name: MayPicks, Type: int  
Name: JunPicks, Type: int  
Name: JulPicks, Type: int  
Name: AugPicks, Type: int  
Name: SepPicks, Type: int  
Name: OctPicks, Type: int  
Name: NovPicks, Type: int  
Name: DecPicks, Type: int  
Name: JanSales, Type: int  
Name: FebSales, Type: int  
Name: MarSales, Type: int  
Name: AprSales, Type: int  
Name: MaySales, Type: int  
Name: JunSales, Type: int  
Name: JulSales, Type: int  
Name: AugSales, Type: int  
Name: SepSales, Type: int  
Name: OctSales, Type: int  
Name: NovSales, Type: int  
Name: DecSales, Type: int  
Name: JanManualPicks, Type: int  
Name: FebManualPicks, Type: int  
Name: MarManualPicks, Type: int  
Name: AprManualPicks, Type: int  
Name: MayManualPicks, Type: int  
Name: JunManualPicks, Type: int  
Name: JulManualPicks, Type: int  
Name: AugManualPicks, Type: int  
Name: SepManualPicks, Type: int  
Name: OctManualPicks, Type: int  
Name: NovManualPicks, Type: int  
Name: DecManualPicks, Type: int  
Name: JanManualSales, Type: int  
Name: FebManualSales, Type: int  
Name: MarManualSales, Type: int  
Name: AprManualSales, Type: int  
Name: MayManualSales, Type: int  
Name: JunManualSales, Type: int  
Name: JulManualSales, Type: int  
Name: AugManualSales, Type: int  
Name: SepManualSales, Type: int  
Name: OctManualSales, Type: int  
Name: NovManualSales, Type: int  
Name: DecManualSales, Type: int  
Name: JanTotalPicks, Type: int  
Name: FebTotalPicks, Type: int  
Name: MarTotalPicks, Type: int  
Name: AprTotalPicks, Type: int  
Name: MayTotalPicks, Type: int  
Name: JunTotalPicks, Type: int  
Name: JulTotalPicks, Type: int  
Name: AugTotalPicks, Type: int  
Name: SepTotalPicks, Type: int  
Name: OctTotalPicks, Type: int  
Name: NovTotalPicks, Type: int  
Name: DecTotalPicks, Type: int  
Name: JanTotalSales, Type: int  
Name: FebTotalSales, Type: int  
Name: MarTotalSales, Type: int  
Name: AprTotalSales, Type: int  
Name: MayTotalSales, Type: int  
Name: JunTotalSales, Type: int  
Name: JulTotalSales, Type: int  
Name: AugTotalSales, Type: int  
Name: SepTotalSales, Type: int  
Name: OctTotalSales, Type: int  
Name: NovTotalSales, Type: int  
Name: DecTotalSales, Type: int  
Name: 13MonthPicks, Type: int  
Name: 13MonthSales, Type: int  
Name: 13MonthLostSales, Type: int  
Name: 13MonthManualPicks, Type: int  
Name: 13MonthManualSales, Type: int  
Name: 13MonthTotalPicks, Type: int  
Name: 13MonthTotalSales, Type: int  
Name: 13MonthTotalLostSales, Type: int  
Name: DateAdded, Type: datetime  
Name: SuggestedOrderMonths, Type: int  
Name: Ignore, Type: int


---   ### PartsPhysicalInventory 

Key: PartsPhysicalInventory,  
Type: View,  
Command: vwIN_SSR_PartsPhysicalInventory,  
HasReturn: false,  
ReturnType:  
DefaultSort: DateCompleted,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: PhysicalInventoryRequestID, Type: int  
Name: BranchID, Type: int  
Name: Branch, Type: varchar(10)  
Name: ExcludeItemsWithZeroAvailable, Type: bit  
Name: SetCountQuantitytoZero, Type: bit  
Name: RequireMaintenanceUpdateOnAllRecords, Type: bit  
Name: PrintSequence, Type: int  
Name: PageBreak, Type: int  
Name: PageBreakPosition, Type: int  
Name: NumberOfWriteInLinesPerPage, Type: int  
Name: StartingSupplier, Type: varchar(20)  
Name: EndingSupplier, Type: varchar(20)  
Name: StartingPartNumber, Type: varchar(30)  
Name: EndingPartNumber, Type: varchar(30)  
Name: StartingBinLocation, Type: varchar(20)  
Name: EndingBinLocation, Type: varchar(20)  
Name: StartingLastReceivedDate, Type: datetime  
Name: EndingLastReceivedDate, Type: datetime  
Name: StartingLastSoldDate, Type: datetime  
Name: EndingLastSoldDate, Type: datetime  
Name: StartingLastCountedDate, Type: datetime  
Name: EndingLastCountedDate, Type: datetime  
Name: IsCompleted, Type: bit  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: PrintQuantityAvailable, Type: bit  
Name: PrintQuantityCommitted, Type: bit  
Name: PrintDetailOfQuantityCommitted, Type: bit  
Name: CoreOptions, Type: varchar(10)  
Name: IsFullInventory, Type: bit  
Name: DateCompleted, Type: datetime  
Name: PartCount, Type: int  
Name: WriteInCount, Type: int  
Name: ReplacementCostDifference, Type: decimal  
Name: AverageCostDifference, Type: decimal  
Name: PrintAlternateBinLocations, Type: bit


---



### PartsPhysicalInventoryDetail 

Key: PartsPhysicalInventoryDetail,  
Type: View,  
Command: vwIN_SSR_PartsPhysicalInventoryDetail,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BranchID, Type: int  
Name: PhysicalInventoryRequestDetailID, Type: int  
Name: PhysicalInventoryRequestID, Type: int  
Name: PartsInventoryDetailID, Type: int  
Name: Sequence, Type: int  
Name: OldQuantity, Type: int  
Name: NewQuantity, Type: int  
Name: IsProcessed, Type: bit  
Name: IsWriteIn, Type: bit  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: LastUpdateUser, Type: varchar(20)  
Name: LastUpdateDate, Type: datetime  
Name: AverageCost, Type: decimal  
Name: InherentCoreAverageCost, Type: decimal  
Name: ReplacementCost, Type: decimal  
Name: InherentCoreReplacementCost, Type: decimal  
Name: QuantityDifference, Type: int  
Name: AverageCostDifference, Type: decimal  
Name: ReplacementCostDifference, Type: decimal  
Name: Supplier, Type: varchar(20)  
Name: PartNumber, Type: varchar(50)  
Name: PartDescription, Type: varchar(50)


---



### PartsAlternateBinLocations

Key: PartsAlternateBinLocations,  
Type: View,  
Command: vwIN_SSR_PartsAlternateBinLocations,  
HasReturn: false,  
ReturnType:  
DefaultSort: PartNumber,  
DefaultPageSize: 100,  
MaxPageSize: 1000,  
Input: null,



#### Output:

Name: BinLocationAlternateID, Type: int  
Name: Branch, Type: varchar(10)  
Name: PartNumber, Type: varchar(50)  
Name: PartsInventoryDetailID, Type: int  
Name: BinLocationID, Type: int  
Name: AlternateBinLocation, Type: varchar(20)  
Name: Sequence, Type: int  
Name: AddUserID, Type: int  
Name: AddUser, Type: varchar(20)  
Name: AddDate, Type: datetime  
Name: UpdateUserID, Type: int  
Name: UpdateUser, Type: varchar(20)  
Name: LastUpdate, Type: datetime
