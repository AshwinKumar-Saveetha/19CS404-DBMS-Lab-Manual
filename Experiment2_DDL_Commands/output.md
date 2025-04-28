**Question 1**
--
Create a table named Employees with the following columns:

EmployeeID as INTEGER
FirstName as TEXT
LastName as TEXT
HireDate as DATE

```sql
CREATE TABLE Employees(EmployeeID INTEGER,FirstName TEXT,LastName TEXT,HireDate DATE)
```

**Output:**


**Question 2**
---
Create a table named Products with the following constraints:
ProductID as INTEGER should be the primary key.
ProductName as TEXT should be unique and not NULL.
Price as REAL should be greater than 0.
StockQuantity as INTEGER should be non-negative.

```sql
CREATE TABLE Products(
ProductID INTEGER PRIMARY KEY,
ProductName TEXT UNIQUE NOT NULL,
Price REAL CHECK(Price>0),
StockQuantity INTEGER Check(StockQuantity>=0)
)
```

**Output:**

![image](https://github.com/user-attachments/assets/7bea2921-c890-461d-a17e-2cbe70131d58)

**Question 3**
---
Create a new table named item with the following specifications and constraints:
item_id as TEXT and as primary key.
item_desc as TEXT.
rate as INTEGER.
icom_id as TEXT with a length of 4.
icom_id is a foreign key referencing com_id in the company table.
The foreign key should cascade updates and deletes.
item_desc and rate should not accept NULL.

```sql
CREATE TABLE item(item_id TEXT PRIMARY KEY,
item_desc TEXT NOT NULL,
rate INTEGER NOT NULL,
icom_id TEXT CHECK(LENGTH(icom_id)=4),
FOREIGN KEY(icom_id) REFERENCES company(com_id) ON UPDATE CASCADE ON DELETE CASCADE
);
```

**Output:**
![image](https://github.com/user-attachments/assets/4572780d-3e3b-45ab-8f15-fc4855128750)

**Question 4**
---
Write a SQL query to Add a new column Country as text in the Student_details table.

Sample table: Student_details

 cid              name             type   notnull     dflt_value  pk
---------------  ---------------  -----  ----------  ----------  ----------
0                RollNo           int    0                       1
1                Name             VARCH  1                       0
2                Gender           TEXT   1                       0
3                Subject          VARCH  0                       0
4                MARKS            INT (  0                       0
```sql
ALTER TABLE Student_details ADD COLUMN Country TEXT;
```

**Output:**

![image](https://github.com/user-attachments/assets/8fc4f66c-5670-40fb-93ee-87a1dde471ba)

**Question 5**
---
Insert all books from Out_of_print_books into Books

Table attributes are ISBN, Title, Author, Publisher, YearPublished
```sql
INSERT INTO Books SELECT * FROM Out_of_print_books;
```

**Output:**

![image](https://github.com/user-attachments/assets/21507e90-7417-4b31-ba26-e9eb02ad284d)

**Question 6**
---
Write a SQL query to add birth_date attribute as timestamp (datatype) in the table customer 

Sample table: customer

 customer_id |   cust_name    |    city    | grade | salesman_id 
-------------+----------------+------------+-------+-------------
        3002 | Nick Rimando   | New York   |   100 |        5001
        3007 | Brad Davis     | New York   |   200 |        5001
        3005 | Graham Zusi    | California |   200 |        5002
```sql
ALTER TABLE customer ADD COLUMN birth_date timestamp;
```

**Output:**

![image](https://github.com/user-attachments/assets/0d12a651-6cda-4738-8ae6-22fba7cc5613)

**Question 7**
---
Insert the below data into the Books table, allowing the Publisher and Year columns to take their default values.

ISBN             Title                 Author
---------------  --------------------  ---------------
978-6655443321   Big Data Analytics    Karen Adams

Note: The Publisher and Year columns will use their default values.
 
```sql
INSERT INTO Books(ISBN,Title,Author) VALUES ("978-6655443321","Big Data Analytics","Karen Adams");
```

**Output:**

![image](https://github.com/user-attachments/assets/d7cb3583-cf2b-4a9f-93cd-28a5cf55cc3a)

**Question 8**
---
In the Cusomers table, insert a record where some fields are NULL, another record where all fields are filled without any NULL values, and a third record where some fields are filled, and others are left as NULL.

CustomerID  Name          Address      City        ZipCode
----------  ------------  ----------   ----------  ----------
306         Diana Prince  Themyscira
307         Bruce Wayne   Wayne Manor  Gotham      10007
308         Peter Parker  Queens                   11375
```sql
INSERT INTO Customers(CustomerID,Name,Address,City,ZipCode) VALUES(306,"Diana Prince","Themyscira",NULL,NULL),(307,"Bruce Wayne","Wayne Mano","Gotham",10007),(308,"Peter Parker","Queens",null,11375);
```

**Output:**

![image](https://github.com/user-attachments/assets/ffb6bb6e-a3d5-4d03-aafa-166819f939b6)


**Question 9**
---
create a table named jobs including columns job_id, job_title, min_salary and max_salary, and make sure that, the default value for job_title is blank and min_salary is 8000 and max_salary is NULL will be entered automatically at the time of insertion if no value assigned for the specified columns.

```sql
CREATE TABLE jobs(job_id,job_title DEFAULT " ", min_salary DEFAULT 8000, max_salary DEFAULT NULL);
```

**Output:**

![image](https://github.com/user-attachments/assets/d5f56677-9be4-4787-b9df-ba017076fa5e)


**Question 10**
---
Create a new table named item with the following specifications and constraints:
item_id as TEXT and as primary key.
item_desc as TEXT.
rate as INTEGER.
icom_id as TEXT with a length of 4.
icom_id is a foreign key referencing com_id in the company table.
The foreign key should set NULL on updates and deletes.
item_desc and rate should not accept NULL.

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)
