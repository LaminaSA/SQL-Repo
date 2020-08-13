## What is SQL? ##
**SQL** stands for Structured Query Language. 

- It is used for managing data in relational database management system which stores data in the form of tables.
- The relationship between data is also stored in the form of tables. 
- SQL statements are used to retrieve and update data in a database
- SQL operates through simple, declarative statements. This keeps data accurate and secure, and it helps maintain the integrity of databases, regardless of size.

**What is a database?**
- An organised repository of data in order to efficiently retrieve data 
- It is held in a computer

**Examples of databases:**
- eCommerce
- Finances
- Customer Bank Accounts
- Sales information

> We must be able to structure tables to contain the right type of information, so that we can query it

**We have to label *raw data* in order to process our data and information efficiently**

---
## Terminology 
- **Column** - Database tables are composed of individual columns corresponding to the attributes of the object
- **Row** - A row consists of one set of attributes corresponding to one instance that a table describes. Also known as Records or Tuples.
- **Table** - A predefined format of rows and columns that define an entity. Also known as a File.
- **Entity** - Anything you want to model in a table
- **DBMS** - A **D**ata **B**ase **M**anagement **S**ystem allows a computer to perform database functions of storing, retrieving, adding, deleting and modifying data.
- **Candidate Key** - Candidates for becoming primary key

> Example: Stud ID, Roll No, and email are candidate keys which helps us to uniquely identify the student record in the table. 
> **StudID** | Roll No | First Name | Last Name | Email
> --- | --- | --- | --- | ---
> 1 | 11 | Tom |Price|abc@gmail.com
> 2 | 12 | Nick | Wright | xyz@gmail.com
> 3 | 13 | Dana | Natan | mno@yahoo.com

**Candidate Key Constraints:**
- It must contain unique values
- Must not contain `null` values
- It should not contain minimum fields to ensure uniqueness
- Uniquely identify each record in a table

- **Composite Key** - A key that has more than one attributes. Refers to cases where more than one column is used to specify the primary key of a table. 

> Example: In the Sales table, there are four columns (attributes) - **cust_id**, **product_code**, **product_count**:

> cust_id | order_id | product_code | product_count
> --- | --- | --- | ---
> CO1 | 0001 | POO7 | 23
> C02 | 0123 | P007 | 19
> C02 | 0123 | P230 | 82
> C01 | 0001 | P890 | 42
> - None of these columns **alone** can play a role of key in this table.
> - The key should be having more than one attributes: **{cust_id, product_code}**


- **Foreign Key** - A key used to link two tables together. Refers to the primary key in another table. 
> Example: In the SalesOrderHeader table, the column **SalesOrderHeader.CurrencyRateID** is a **foreign** key since it is related to the **CurrencyRate.CurrencyRateID.** **CurrencyRate.CurrencyRateID** is the primary key of the **CurrencyRate** table.
>![foreign_key](../../images/foreign_key.webp)

- **Primary Key** - Uniquely identifies each record in the table 
> *Most* tables should have a primary key 
> Each table can have more than one column which is part of its Primary Key (composite key) e.g. Order No + Order Line Number
> The DMBS will enforce the uniqueness of the Primary Key, not allowing repeated records to exist in the records.
> The primary key for each table is stored in an index, used to enforce the uniqueness requirement. 

**Primary Key Constraints**
- A primary key must be unique 
- Must always have an entry 
    - cannot be blank or `NULL`
- The value must never change 
- Each table may have a maximum of one Primary Key (or one composite primary key)

- **Junction Table**
    - Also known as a Bridge Table or Join Table, Junction Table contains references to two groups 
    - Used when dealing with many-to-many relationships in SQL database.

> Example: You have a list of students and a list of classes. There's a **many-to-many** relationship between the students and their classes:

> - Each student can take multiple classes
> - Each class have have multiple students enrolled
> - A junction table is useful if we want to store information about each student's grades or which semester that student took the class

---
## Types of Database
- **Flat-File Database**
    - Stores everything in one Table. Good for small numbers of records related to a single topic.
- **Relational Database**
    - Gives you the ability to separate masses of data into numerous tables.
    - They are linked to each other through the use of keys.
- **Big Data**
    - MongoDB, Vertica, etc.
    - Used for Data Analytics and Business Intelligence
    - Digital Age and Internet of Thing