# Basic-SQL-Commands
// Basic SQL Commands

## 1 Select All
```
SELECT *
FROM orderlist
```
## 2 Select All (Distinct)
```
SELECT DISTINCT Invoice
FROM orderlist
```
## 3 Where
```
SELECT *
FROM orderlist
WHERE id = 25
```
## 4 And, OR, NOT
```
SELECT *
FROM orderlist
WHERE Id = 10 AND Invoice = 'abcxyz'
```
```
SELECT *
FROM orderlist
WHERE Id = 10 OR Invoice = 'abcxyz'
```
```
SELECT *
FROM orderlist
WHERE NOT RefTrx = 'AAE0M3JW8Q'
```
## 5 Order By
```
SELECT *
FROM orderlist
ORDER BY Id ASC
```
```
SELECT *
FROM orderlist
ORDER BY Id DESC
```
## 6 Insert Into
```
INSERT INTO orderlist (`Id`,`Invoice`,`RefTrx`)
VALUES (1000, 'testInvoiceId', 'testRefTrx');
```
## 7 Update
```
UPDATE orderlist
SET RefTrx = 'updatedRefId', Invoice = 4.1254
WHERE id = 5;
```
## 8 Delete
```
DELETE
FROM orderlist
WHERE Id = 7;
```
## 9 Avg, Min, Max, Count, Sum
```
SELECT AVG(Amount)
FROM paystation
WHERE Payment_Method = 'bKash';
```
```
SELECT MIN(Amount)
FROM paystation
WHERE Payment_Method = 'bKash';
```
```
SELECT MAX(Amount)
FROM paystation
WHERE Payment_Method = 'bKash';
```
```
SELECT SUM(Amount)
FROM paystation
WHERE Payment_Method = 'bKash';
```
```
SELECT COUNT(Amount)
FROM paystation
WHERE Payment_Method = 'bKash';
```
## 10 Like (Starts with 015)
```
SELECT *
FROM paystation
WHERE Customer_Mobile LIKE '015%';
```
## 11 Like (Contains 015)
```
SELECT *
FROM paystation
WHERE Customer_Mobile LIKE '%015%';
```
## 12 Like (Starts with 0 and has at least 2 characters)
```
SELECT *
FROM paystation
WHERE Customer_Mobile LIKE '0_';
```
## 13 In (Select where contains these values)
```
SELECT * 
FROM paystation
WHERE Payment_Method IN ('Nagad', 'Rocket');
```
```
SELECT * 
FROM paystation
WHERE Payment_Method IN ('Nagad', 'Rocket');
```
## 14 In (Select where contains values from another table)
```
SELECT * 
FROM paystation
WHERE Payment_Method IN (SELECT Payment_Method FROM anothertable);
```
## 15 Between
```
SELECT * 
FROM paystation
WHERE Amount BETWEEN 0 AND 505
```
## 16 Alias
```
SELECT Amount AS 'Temp table title'
FROM paystation
WHERE 1
```
## 17 Join
```
SELECT table1.id, table2.name
FROM table1
INNER JOIN table2 ON table1.id = taabl2.id
```
```
SELECT table1.id, table2.name
FROM table1
LEFT JOIN table2 ON table1.id = taabl2.id
```
```
SELECT table1.id, table2.name
FROM table1
RIGHT JOIN table2 ON table1.id = taabl2.id
```
```
SELECT table1.id, table2.name
FROM table1
CROSS JOIN table2 ON table1.id = taabl2.id
```
## 18 Union
```
SELECT id FROM table1
UNION
SELECT id FROM table2
```
## 19 Alter
```
ALTER TABLE paystation
ADD name varchar(255)
```
```
ALTER TABLE paystation
DROP COLUMN name;
```
```
ALTER TABLE paystation
MODIFY COLUMN Action varchar(255);
```
