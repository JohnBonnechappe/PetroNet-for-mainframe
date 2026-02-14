# PetroNet-for-mainframe
A system for a distributor to manage their stocks and logistics. Written in COBOL DB2 for the ZOS platform.

This system is for a distritbotor to manage their stock inventories and customers at their various depots. STock can be received into the inventory, and is then sold to customers at that depot. All stock receipts are tracked as well as sales, transfers out, and stock adjustments.

The system is written for the IBM ZOS environment using COBOL, DB2 and interfaces in REXX and CICS.

A distributor can have many locations. At each location there are stock levels and customers.

Database tables are set up in a DB2 schema using JCL running SQL scripts. Initial data setup is via DB2 loads into database tables from datasets in text format. Online panels are provided to updatate this data.

Principle tables are
DISTSHIP_PARAM_TBL    to define parameters for the distributorship
LOCN_TBL              to define locations where stock may be help
PROD_TBL              describes products
STOCK_HOLDING_TBL     defines stock levels at each location
CUST_TBL              list of customers
STOCK_RCPT_TBL        to record stock receipts
SALES_DOCKET_HDR_TBL  header records for stock sales
SALES_DOCKET_ITEM_TBL line items for stock sales
