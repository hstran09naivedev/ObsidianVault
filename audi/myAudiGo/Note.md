BFF stands for Backend for Frontend architecture? Yes
**Remind Phillip about:**
Git instruction for implementation and code review
Also how to deploy for testing

Checklist before liquibase changelog as a golden state
- [x]  Check **collations**, charset, engine for **all tables/columns** ->
**collations**
List all the foreign_key columns and its referencing columns:
CUSTOMER_ACCESS,USERID,CACCESS_CU_FK
CUSTOMER_ACTION,USERID,CA_CU_FK
CUSTOMER_DATA,USERID,FK_CD_C
CUSTOMER_PARTNER,USERID,CP_CU_FK
TB_CONTRACT,USERID,FK_TBC_C
VEHICLE_ACTION,USERID,VA_CU_FK
is string column (varchar) -> COLLATION IS IMPORTANT -> NEED TO be explicit in Changeset
**Engine** for tables: Let the it automatically set for tables (usually innoDB engine)
**Charset**: Confirm dev team about the charset in livestage?
- [x]  Check **auto_increment**
For existing auto_increment (and we don't add/modify any more), It will not be affected.
- [x]  Check **ENUM/SET definitions**
-> There is no ENUM/SET type for any column that I could found in the DB locally
- [x]  Check for **comments**, **generated columns**
-> MAKE nonsense
- [x]  For **PARTITIONED tables**: verify partitioning info is preserved
-> Found nothing
- [ ]  Review **foreign key ON UPDATE/DELETE** rules
-> Saved in the csv file -> Updated in the 1.sql
- [ ]  Use mysqldump to confirm the script

