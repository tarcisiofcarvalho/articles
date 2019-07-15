# SQL Language

### Definitions

*   **DDL (Data Definition Language)**: It defines the database structure with CREATE, ALTER, TRUNCATE, etc.
*   **DML (Data Manipulation Language)**: It defines the database data management as SELECT, INSERT, UPDATE, DELETE, etc.
*   **DCL (Data Control Language)**: Deal with access control as GRANT and REVOKE
*   **TCL (Transaction Control Language)**: It defines transactions commands as COMMIT and ROLLBACK

### Create Table

```sql
CREATE TABLE Persons (
    id int,
    lastName varchar(255),
    firstName varchar(255)
);
```

### Insert

```sql
INSERT INTO Persons (id, lastName, firstName)
VALUES (1, 'Carvalho', 'Tarcisio');
```

### Update

```sql
UPDATE Persons
SET lastName='Franco de Carvaho'
WHERE id=1;
```

### Delete

```sql
DELETE FROM Persons 
WHERE id=1;
```
