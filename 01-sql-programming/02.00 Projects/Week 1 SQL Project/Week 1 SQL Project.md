# SQL-Week-One-Practice

Development actors and governments often deal with several sources of data that are stored in different places and in different formats. Part of A data analyst's work is helping clients manage their data assets and learn from the inter-connections. In this example, the client has asked you to extract data related to one of their programmes in Somalia, calculate key indicators from such data, and export it in a format that is used by their reporting platform. 

1) Create the following three database tables [run tablegen.sql script](https://drive.google.com/file/d/1N2CC2gtjQEPNuyrM7wIiO0P-ipqejgI6/view?usp=sharing)

Table|Description|
-----|-----------|
Village location | Where the projects are run and are associated with geographic coordinates|
Beneficiary Partner Data| Each Partner records the number of projects in a subset of villages and records the number of beneficiaries|
Jurisdiction Hierachy| Village is the lowest then District then Region|

2. Write a SQL script that creates the following summary tables (can be tables or views): 

  a) ****District_summary****. 

> i) District Name 

> ii) Region Name 

> iii) No. of Individual Beneficiaries (1HH = 6 Individuals)

> iv) No. of Individual Beneficiaries / Total District Population

  b) ****Partner_summary**** 
 
> i) Partner Name

> ii) No. of Villages reached by partner 

> iii) No. of Districts reached by partner


