# *MySQL Commands*

### 1. Create Database

This project is a **childcare** inquiry  application that allows users to **create**, **select**, **update** and **delete** inquiry details.
***
### 2. Defining Colums
 
 - 1.ID : `INT`
 - 2. Name : `VARCHAR(50)`
 - 3. Phone Number `VARHAR(100)`
 - 4. Email `VARHAR(50)`
 - 5. Child Name`VARHAR(50)`
 - 6. Child Age `INT`
 
### 3.Create Table
```sql
CREATE TABLE childcare
(id INT NOT NULL AUTO_INCREMENT,
 name Varchar(50) NOT NULL,
 phonenumber Varchar(100),
 email Varchar(50) NOT NULL,
 childname Varchar(50) NOT NULL,
 childage INT,
 PRIMARY KEY (id)
);
```

### 4. Insert Into Table

**Inserting values in the table**

```sql
INSERT INTO childcare (
id,
name,
phonenumber,
email,
childname,
childage
) VALUES (
1,
'Muneer Basha',
'778301577',
'MuneerBasha@gmail.com',
'Saifali',
2
);
```
 - **Inserting Multi Values in the table**
 
 ```sql
 INSERT INTO childcare (
 id,
name,
phonenumber,
email,
childname,
childage
) VALUES (
2,
'Mehaboob'
'778301612',
'Mehaboob@gmail.com',
'Roshan',
3
),(
3,
'Harish Kumar'
'956301612',
'Harish@gmail.com',
'Kajol',
4
),(
4,
'Lakshmi'
'7783085612',
'Lakshmi@gmail.com',
'Jasmin',
5
);
 ```
### 5. Select

#### Commands

- SELECT
- FROM 
- WHERE

#### Example :

> **Select all from table**

```sql
SELECT * FROM childcare
```
> **Select specific data by its id**

```sql
SELECT * FROM childcare WHERE id = 4
```
> **Selecting childnames from table**
```sql
SELECT childname FROM childcare
```
> **Selecting name of the parent by its email**

```sql
SELECT name FROM childcare WHERE email = 'MuneerBasha@gmail.com'
```


> **Selecting all inquiries with a  amount greaterthan 48000**

```sql
SELECT *  FROM childcare WHERE amount>10000
```
> **Selecting parentname,childname,childage from table**

```sql
SELECT name,childname,childage FROM childcare
```
### Update

#### Commands

- UPDATE
- SET
- WHERE
#### EXAMPLES :

> **Update email from table by its id**

```sql
UPDATE childcare SET email = 'Muneer@gmail.com' WHERE id = 1
```

> **Update the childname of speifi enquiry by childage

```sql
UPDATE childcare SET childname = 'Sony' WHERE childage = 3
```

### DELETE

#### Commands 

- DELETE FROM
- WHERE

#### EXAMPLE

> **Delete a specific inquiry by its id**

```sql
DELETE FROM childcare WHERE id = 4 
```

> **Delete all inquiries from the table

```sql
DELETE FROM childcare
```
### Using `AS`

We use as in **mysql** cmd it will change the **column name temporary** while checking preview.

#### EXAMPLE

```sql 
SELECT childname AS name FROM childcare 
```

### Aggregate Functions

**AVG , SUM , COUNT , MAX , MIN** we use this aggregate functions to check the Average,Sum(total),Count(count of rows),Minimum,Maximum values of data.
This are only apply on **Number** data type.

#### EXAMPLE

```sql
SELECT AVG(amount) FROM childcare WHERE status = 'Approved'
SELECT MAX(amount) FROM childcare WHERE status = 'Approved'
SELECT MIN(amount) FROM childcare WHERE status = 'Approved'
SELECT SUM(amount) FROM childcare WHERE status = 'Approved'
SELECT COUNT(amount) FROM childcare WHERE status = 'Approved'
```
