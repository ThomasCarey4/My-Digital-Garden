---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/databases/old/sql/"}
---

- **Data Definition Language (DDL)**
- **Data Manipulation Language (DML)**
#### Commands
>[!tip] 
>New lines can be put anywhere (obv not mid word) and don’t effect the end result
```sqlite
CREATE TABLE PrivateOwner(
ownerNo INTEGER PRIMARY KEY,
fName TEXT,
lName TEXT,;
-- Create an example table
```
```sqlite
ALTER TABLE Staff ALTER lName
DROP DEFAULT;
-- Delete the DEFAULT value for the lName column
```
```sqlite
ALTER TABLE PrivateOwner
ADD phoneNo TEXT;
-- Add phoneNo coloumn
```
```sqlite
DROP TABLE PrivateOwner;
-- Delete the table
```

```sqlite
INSERT INTO PrivateOwner
VALUES (12, 'John', 'Smith');
-- Add new row to a table
```
```sqlite
INSERT INTO PrivateOwner (ownerNo, fName)
VALUES (17, 'Kevin');
-- Add new row without all the data
```
```sqlite
DELETE FROM PrivateOwner
WHERE fName = 'Kevin';
-- Delete ALL rows with first name 'Kevin'
```
```sqlite
UPDATE PrivateOwner
SET lName = 'Cena'
WHERE fName = 'John' OR ownerNo = 12;
-- Update a row
```

```sqlite
SELECT fName, lName
FROM PrivateOwner;
-- Show table with only fName and lName columns
```
```sqlite
SELECT
DISTINCT fName
FROM PrivateOwner;
-- Select without duplicates
```
```sqlite
SELECT fName, lName, ownerNo/12
FROM PrivateOwner;
-- Show table where all ownerNo's are modified
```
```sqlite
SELECT fName AS 'First Name',
lName AS 'Last Name'
FROM Private Owner
-- Change the displayed names of the columns
```
#TODO SELECT WHERE
#TODO SELECT ORDER BY
#TODO SELECT GROUP BY
#TODO SELECT GROUP BY, HAVING
