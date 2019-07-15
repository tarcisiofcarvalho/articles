# SQL Commands

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
