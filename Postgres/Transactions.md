# Starting and Ending of a transaction

A Transaction is a group of SQL Commands. Transaction means all or nothing and follows ACID properties. 

- To start **transaction** in PostgreSQL write:
  - `BEGIN` and then write the commands
  - `ROLLBACK`to cancel the transaction
  - `COMMIT` to save the changes in the transaction
 
- To define a `SAVEPOINT` do:
  - `SAVEPOINT SP_ids`: where **SP_ids** is the name of the savepoint
  - `ROLLBACK TO SAVEPOINT SP_ids`: to rollback to the save point **SP_ids**
  - `RELEASE SAVEPOINT SP_ids`: To delete a savepoint
 
- System Column
  - `xmin` : Shows insert or update operation
  - `xmax` : Shows delete operation
  - `ctid` 
  - To creata a table using `WITH OIDS` during create table command: unique Id for each row
