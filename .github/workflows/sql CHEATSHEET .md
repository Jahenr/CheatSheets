**SQL** Cheat Sheet![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.001.png)

In this guide, you ll find a useful cheat sheet that documents some of the more commonly used elements of SQL, and even a few of the less common. Hopefully, it will help developers   both beginner and experienced level   become more proficient in their understanding of the SQL language.

Use this as a quick reference during development, a learning aid, or even print it out and bind it if you d prefer (whatever works!).

But before we get to the cheat sheet itself, for developers who may not be familiar with SQL, let s start with 

**Table of Contents![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.002.png)**

**03 What is SQL**

7  **SQL vs MySQL**
7  **Installin  MySQL**
7  **Usin  MySQL**

**11 Cheat Sheet**

20  **Comments**
20  **MySQL Data Types**

**25 Operators**

**27 Functions**

36  **Wildcard Characters**
36  **Keys**
39  **Indexes**
39  **Joins**
42  **View**
42  **Conclusions**

**WebsiteSetup.or**  - MySQL Cheat Sheet

43

**What is SQL**

SQL stands for Structured Query Language. It s the language of choice on today s web for storing, manipulating and retrieving data within relational databases. Most, if not all of the websites you visit will use it in some way, including this one.

Here s what a basic relational database looks like. This example in particular stores e-commerce information, specifically the products on sale, the users who buy them, and records of these orders which link these 2 entities.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.003.jpeg)Using SQL, you are able to interact with the database by writing queries, which when executed, return any results which meet its criteria.

Here s an example query:-

**SELECT** \* **FROM** users;

Using this SELECT statement, the query selects all data from all columns in the user s table. It would then return data like the below, which is typically called a results set:-

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.004.jpeg)If we were to replace the asterisk wildcard character (\*) with specific column names instead,  only the data from these columns would be returned from the query.

**SELECT** first\_name, last\_name **FROM** users;

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.005.png)

We can add a bit of complexity to a standard SELECT statement by adding a WHERE clause, which allows you to filter what gets returned.

**SELECT** \* **FROM** products **WHERE** stock\_count <= 10 **ORDER BY** stock\_count **ASC**;

This query would return all data from the products table with a stock\_count value of less than 10 in its results set. The use of the ORDER BY keyword means the results will be ordered using the stock\_count column, lowest values to highest.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.006.jpeg)

Using the INSERT INTO statement, we can add new data to a table. Here s a basic example adding a new user to the users table:-

**INSERT** **INTO** users (first\_name, last\_name, address, email)

**VALUES** (‘Tester’, ‘Jester’, ‘123 Fake Street, Sheffield, United Kingdom’, ‘test@lukeharrison.dev’);

Then if you were to rerun the query to return all data from the user s table, the results set would look like this:

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.007.jpeg)

Of course, these examples demonstrate only a very small selection of what the SQL language is capable of.

**SQL vs MySQL**

You may have heard of MySQL before. It s important that you don t confuse this with SQL itself, as there s a clear difference.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.008.jpeg)

SQL is the language. It outlines syntax that allows you to write queries that manage relational databases. Nothing more.

MySQL meanwhile is a database system that runs on a server. It implements the SQL language, allowing you to write queries using its syntax to manage MySQL databases.

In addition to MySQL, there are other systems that implement SQL. Some of the more popular ones include:

PostgreSQL

SQLite

Oracle Database Microsoft SQL Server

**Installin  MySQL**

**Windows**

The recommended way to install MySQL on Windows is by using the installer you can download from the MySQL website.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.009.jpeg)

**MacOS**

On macOS, the recommended way to install MySQL is using native packages, which sounds a lot more complicated than it actually is. Essentially, it also involves just downloading an installer.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.010.jpeg)

Alternatively, If you prefer to use package managers such as Homebrew, you can install MySQL like so:

brew install mysql

Whilst if you need to install the older MySQL version 5.7, which is still widely used today on the web, you can:

brew install mysql@5.7

**Usin  MySQL**

With MySQL now installed on your system, to get up and going as quickly as possible writing SQL queries, it s recommended that you use an SQL management application to make managing your databases a much simpler, easier process.

There are lots of apps to choose from which largely do the same job, so it s down to your own personal preference on which one to use:

MySQL Workbench is developed by Oracle, the owner of MySQL.

HeidiSQL (Recommended Windows) is a free, open-source app for Windows. For macOS and Linux users, Wine is first required as a prerequisite.

phpMyAdmin is a very popular alternative that operates in the web browser.

Sequel Pro (Recommended macOS) is a macOS  only alternative and our favorite thanks to its clear and easy to use interface.

When you re ready to start writing your own SQL queries, rather than spending time creating your own database, consider importing dummy data instead.

The MySQL website provides a number of dummy databases that you can download free of charge and then import into your SQL app.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.011.jpeg)

Our favorite of these is the world database, which provides some interesting data to practice writing SQL queries for. Here s a screenshot of its country table within Sequel Pro.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.012.jpeg)

This example query returns all countries with Queen Elizabeth II as their head of state    .

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.013.jpeg)

Whilst this one returns all European countries with a population of over 50million along with their capital city and its population.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.014.jpeg)

**Cheat Sheet**

**Keywords**

A collection of keywords used in SQL statements, a description, and where appropriate an example. Some of the more advanced keywords have their own dedicated section later in the cheat sheet.

Where MySQL is mentioned next to an example, this means this example is only applicable to MySQL databases (as opposed to any other database system).



|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**ADD**|<p>Adds a new column to an existing table. </p><p>**Example**:A dds a new column named  email\_address  to a table named  users .</p><p>ALTER TABLE users</p><p>ADD email\_address varchar(255);</p>|
|**ADD CONSTRAINT**|<p>It creates a new constraint on an existing table, which is used to specify rules for any data in the table.</p><p>**Example**:A dds a new PRIMARY KEY constraint named  user  on columns ID and SURNAME.</p><p>ALTER TABLE users</p><p>ADD CONSTRAINT user PRIMARY KEY (ID, SURNAME);</p>|
|**ALTER TABL**|<p>Adds, deletes or edits columns in a table. It can also be used to add and delete constraints in a table, as per the above.</p><p>**Example**:A dds a new boolean column called  approved  to a table named  deals .</p><p>ALTER TABLE deals</p><p>**E** ADD approved boolean;</p><p>**Example 2**:Deletes the  appr oved  column from the  deals  table</p><p>ALTER TABLE deals DROP COLUMN approved;</p>|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**ALTER COLUMN**|<p>Changes the data type of a table s column.</p><p>**Example**:In the  user s  table, make the column  incept\_date  into a  datetime  type.</p><p>ALTER TABLE users</p><p>ALTER COLUMN incept\_date datetime;</p>|
|**ALL**|<p>Returns true if all of the subquery values meet the passed condition. **Example**:Returns the user s with a higher number of tasks than the user with the highest number of tasks in the HR department (id 2)</p><p>SELECT first\_name, surname, tasks\_no FROM users</p><p>WHERE tasks\_no > ALL (SELECT tasks FROM user WHERE department\_id = 2);</p>|
|**AND**|<p>Used to join separate conditions within a WHERE clause. **Example**:Returns events located in London, United Kingdom</p><p>SELECT \* FROM events</p><p>WHERE host\_country='United Kingdom' AND host\_ city='London';</p>|
|**ANY**|<p>Returns true if any of the subquery values meet the given condition. **Example**:Returns pr oducts from the products table which have received orders   stored in the orders table   with a quantity of more than 5.</p><p>SELECT name FROM products</p><p>WHERE productId = ANY (SELECT productId FROM orders WHERE quantity > 5);</p>|
|**AS**|<p>Renames a table or column with an alias value which only exists for the duration of the query.</p><p>**Example**:Aliases nor th\_east\_user\_subscriptions column</p><p>SELECT north\_east\_user\_subscriptions AS ne\_subs FROM users</p><p>WHERE ne\_subs > 5;</p>|
|**ASC**|Used with ORDER BY to return the data in ascending order. **Example**:A pples, Bananas, Peaches, Raddish|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**BETWEEN**|<p>Selects values within the given range.</p><p>**Example 1**:Selects stoc k with a quantity between 100 and 150.</p><p>SELECT \* FROM stock</p><p>WHERE quantity BETWEEN 100 AND 150;</p><p>**Example 2**:Selects stoc k with a quantity NOT between 100 and 150. Alternatively, using the NOT keyword here reverses the logic and selects values outside the given range.</p><p>SELECT \* FROM stock</p><p>WHERE quantity NOT BETWEEN 100 AND 150;</p>|
|**CASE**|<p>Change query output depending on conditions.</p><p>**Example**:Returns user s and their subscriptions, along with a new column called activity\_levels that makes a judgement based on the number of subscriptions.</p><p>SELECT first\_name, surname, subscriptions</p><p>CASE WHEN subscriptions > 10 THEN 'Very active' WHEN Quantity BETWEEN 3 AND 10 THEN 'Active' ELSE 'Inactive'</p><p>END AS activity\_levels</p><p>FROM users;</p>|
|**CHECK**|<p>Adds a constraint that limits the value which can be added to a column. **Example 1 (MySQL)**:Makes sur e any users added to the users table are 18 or over.</p><p>CREATE TABLE users ( first\_name varchar(255), age int,</p><p>CHECK (age>=18)</p><p>); </p><p>**Example 2 (MySQL)**:A dds a check after the table has already been created.</p><p>ALTER TABLE users ADD CHECK (age>=18);</p>|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**CREATE DATABASE**|<p>Creates a new database.</p><p>**Example**:Cr eates a new database named  websitesetup .</p><p>CREATE DATABASE websitesetup;</p>|
|**CREATE TABLE**|<p>Creates a new table .</p><p>**Example**:Cr eates a new table called  users  in the  websitesetup  database.</p><p>CREATE TABLE users ( id int,</p><p>first\_name varchar(255), surname varchar(255), address varchar(255), contact\_number int</p><p>);</p>|
|**DEFAULT**|<p>Sets a default value for a column;</p><p>**Example 1 (MySQL)**:Cr eates a new table called Products which has a name column with a default value of  Placeholder Name  and an available\_ from column with a default value of today s date.</p><p>CREATE TABLE products (</p><p>id int,</p><p>name varchar(255) DEFAULT 'Placeholder Name', available\_from date DEFAULT GETDATE()</p><p>); </p><p>**Example 2 (MySQL)**:T he same as above, but editing an existing table.</p><p>ALTER TABLE products</p><p>ALTER name SET DEFAULT 'Placeholder Name', ALTER available\_from SET DEFAULT GETDATE();</p>|
|**DELETE**|<p>Delete data from a table.</p><p>**Example**:Remo ves a user with a user\_id of 674.</p><p>DELETE FROM users WHERE user\_id = 674;</p>|
|**DESC**|Used with ORDER BY to return the data in descending order. **Example**:Rad dish, Peaches, Bananas, Apples|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**DROP COLUMN**|<p>Deletes a column from a table.</p><p>**Example**:Remo ves the first\_name column from the users table.</p><p>ALTER TABLE users DROP COLUMN first\_name</p>|
|**DROP DATABASE**|<p>Deletes the entire database.</p><p>**Example**:Deletes a database named  w ebsitesetup .</p><p>DROP DATABASE websitesetup;</p>|
|**DROP DEFAULT**|<p>Removes a default value for a column.</p><p>**Example (MySQL)**:Remo ves the default value from the  name  column in the  products  table.</p><p>ALTER TABLE products</p><p>ALTER  COLUMN name  DROP  DEFAULT;</p>|
|**DROP TABLE**|<p>Deletes a table from a database. **Example**:Remo ves the users table.</p><p>DROP TABLE users;</p>|
|**EXISTS**|<p>Checks for the existence of any record within the subquery, returning true if one or more records are returned.</p><p>**Example**:Lists an y dealerships with a deal finance percentage less than 10.</p><p>SELECT dealership\_name FROM dealerships</p><p>WHERE EXISTS (SELECT deal\_name FROM deals WHERE dealership\_id = deals.dealership\_id AND finance\_ percentage < 10);</p>|
|**FROM**|<p>Specifies which table to select or delete data from. **Example**:Selects data fr om the users table.</p><p>SELECT area\_manager FROM area\_managers</p><p>WHERE EXISTS (SELECT ProductName FROM Products WHERE area\_manager\_id = deals.area\_manager\_id AND Price < 20);</p>|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**IN**|<p>Used alongside a WHERE clause as a shorthand for multiple OR condition So instead of:</p><p>SELECT \* FROM users</p><p>WHERE country = 'USA' OR country = 'United Kingdom' OR country = 'Russia' OR country = 'Australia';</p><p>You can use: </p><p>SELECT \* FROM users</p><p>WHERE country IN ('USA', 'United Kingdom', 'Russia', 'Australia');</p>|
|**INSERT INTO**|<p>Add new rows to a table. **Example**:A dds a new vehicle.</p><p>INSERT INTO cars (make, model, mileage, year) VALUES ('Audi', 'A3', 30000, 2016);</p>|
|**IS NULL**|<p>Tests for empty (NULL) values.</p><p>**Example**:Returns user s that haven t given a contact number.</p><p>SELECT \* FROM users</p><p>WHERE contact\_number IS NULL;</p>|
|**IS NOT NULL**|The reverse of NULL. Tests for values that aren t empty / NULL.|
|**LIKE**|<p>Returns true if the operand value matches a pattern. **Example**:Returns tr ue if the user s first\_name ends with  son .</p><p>SELECT \* FROM users</p><p>WHERE first\_name LIKE '%son';</p>|
|**NOT**|<p>Returns true if a record DOESN T meet the condition. **Example**:Returns tr ue if the user s first\_name doesn t end with  son .</p><p>SELECT \* FROM users</p><p>WHERE first\_name NOT LIKE '%son';</p>|
|**OR**|<p>Used alongside WHERE to include data when either condition is true. **Example**:Returns user s that live in either Sheffield or Manchester.</p><p>SELECT \* FROM users</p><p>WHERE city = 'Sheffield' OR 'Manchester';</p>|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**ORDER BY**|<p>Used to sort the result data in ascending (default) or descending order through the use of ASC or DESC keywords.</p><p>**Example**:Returns countries in alphabetical or der.</p><p>SELECT \* FROM countries ORDER BY name;</p>|
|**ROWNUM**|<p>Returns results where the row number meets the passed condition. **Example**:Returns the top 10 countries fr om the countries table.</p><p>SELECT \* FROM countries WHERE  ROWNUM <=  10;</p>|
|**SELECT**|<p>Used to select data from a database, which is then returned in a results set. **Example 1**:Selects all co lumns from all users.</p><p>SELECT \* FROM users;</p><p>**Example 2**: Selects the first\_name and surname columns from all users.xx</p><p>SELECT first\_name, surname FROM users;</p>|
|**SELECT DISTINCT**|<p>Sames as SELECT, except duplicate values are excluded. **Example**:Cr eates a backup table using data from the users table.</p><p>SELECT \* INTO usersBackup2020 FROM users;</p>|
|**SELECT INT**|<p>Copies data from one table and inserts it into another.</p><p>**Example**:Returns all countries fr om the users table, removing any duplicate **O**values (which would be highly likely)</p><p>SELECT DISTINCT country from users;</p>|
|**SELECT TOP**|<p>Allows you to return a set number of records to return from a table. **Example**:Returns the top 3 car s from the cars table.</p><p>SELECT TOP 3 \* FROM cars;</p>|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**SET**|<p>Used alongside UPDATE to update existing data in a table. **Example**:Updates the value and quantity values f or an order with an id of 642 in the orders table.</p><p>UPDATE orders</p><p>SET value = 19.49, quantity = 2 WHERE id = 642;</p>|
|**SOME**|Identical to ANY.|
|**TOP**|<p>Used alongside SELECT to return a set number of records from a table. **Example**:Returns the top 5 user s from the users table.</p><p>SELECT TOP 5 \* FROM users;</p>|
|**TRUNCATE TABLE**|<p>Similar to DROP, but instead of deleting the table and its data, this deletes only the data.</p><p>**Example**:Empties the sessions tab le, but leaves the table itself intact.</p><p>TRUNCATE TABLE sessions;</p>|
|**UNION**|<p>Combines the results from 2 or more SELECT statements and returns only distinct values.</p><p>**Example**:Returns the cities fr om the events and subscribers tables.</p><p>SELECT city FROM events UNION</p><p>SELECT city from subscribers;</p>|
|**UNION ALL**|The same as UNION, but includes duplicate values.|


|**SQL Keywords**|
| - |
|**Keyword**|**Description**|
|**UNIQUE**|<p>This constraint ensures all values in a column are unique.</p><p>**Example 1 (MySQL)**:A dds a unique constraint to the id column when creating a new users table.</p><p>CREATE TABLE users (</p><p>id int NOT NULL,</p><p>name varchar(255) NOT NULL, UNIQUE (id)</p><p>); </p><p>**Example 2 (MySQL)**:Alter s an existing column to add a UNIQUE constraint.</p><p>ALTER TABLE users ADD UNIQUE (id);</p>|
|**UPDATE**|<p>Updates existing data in a table.</p><p>**Example**:Updates the mileage and ser viceDue values for a vehicle with an id of 45 in the cars table.</p><p>UPDATE cars</p><p>SET mileage = 23500, serviceDue = 0 WHERE id = 45;</p>|
|**VALUES**|<p>Used alongside the INSERT INTO keyword to add new values to a table. **Example**:A dds a new car to the cars table.</p><p>INSERT INTO cars (name, model, year) VALUES ('Ford', 'Fiesta', 2010);</p>|
|**WHERE**|<p>Filters results to only include data which meets the given condition. **Example**:Returns or ders with a quantity of more than 1 item.</p><p>SELECT \* FROM orders WHERE quantity > 1;</p>|
**Comments**

Comments allow you to explain sections of your SQL statements, or to comment out code and prevent its execution.

In SQL, there are 2 types of comments, single line and multiline.

**Sin le Line Comments**

Single line comments start with  . Any text after these 2 characters to the end of the line will be ignored.

-- My Select query SELECT \* FROM users;

**Multiline Comments**

Multiline comments start with /\* and end with \*/. They stretch across multiple lines until the closing characters have been found.

/\*

This is my select query.

It grabs all rows of data from the users table \*/

SELECT \* FROM users;

/\*

This is another select query, which I don’t want to execute yet

SELECT \* FROM tasks; \*/

**MySQL Data Types**

When creating a new table or editing an existing one, you must specify the type of data that each column accepts.

In the below example, data passed to the id column must be an int, whilst the first\_name column has a VARCHAR data type with a maximum of 255 characters.

CREATE TABLE users (  ![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.015.png)   id int,

`    `first\_name varchar(255) );

**Strin  Data Types**

**Strin  Data Types**

**Data Type Description**

Fixed length string which can contain letters, numbers and special **CHAR(size)** characters. The size parameter sets the maximum string length, from 

0   255 with a default of 1.

Variable length string similar to CHAR(), but with a maximum string **VARCHAR(size)**

length range from 0 to 65535.

**BINARY(size)** Similar to CHAR() but stores binary byte strings. **VARBINARY(size)** Similar to VARCHAR() but for binary byte strings.

**TINYBLOB** Holds Binary Large Objects (BLOBs) with a max length of 255 bytes.

Holds a string with a maximum length of 255 characters. Use **TINYTEXT**

VARCHAR() instead, as it s fetched much faster.

Holds a string with a maximum length of 65535 bytes. Again, better to **TEXT(size)**

use VARCHAR().

Holds Binary Large Objects (BLOBs) with a max length of 65535 **BLOB(size)**

bytes.

**MEDIUMTEXT** Holds a string with a maximum length of 16,777,215 characters.

**Strin  Data Types**

**Data Type Description**

Holds Binary Large Objects (BLOBs) with a max length of 16,777,215 **MEDIUMBLOB**

bytes.

**LONGTEXT** Holds a string with a maximum length of 4,294,967,295 characters.

Holds Binary Large Objects (BLOBs) with a max length of **LONGBLOB**

4,294,967,295 bytes.

A string object that only has one value, which is chosen from a list of 

values which you define, up to a maximum of 65535 values. If a value 

is added which isn t on this list, it s replaced with a blank value instead. **ENUM(a, b, c,** 

Think of ENUM being similar to HTML radio boxes in this regard.

**etc )**

CREATE TABLE tshirts (color ENUM(‘red’, ‘green’, ‘blue’, ‘yellow’, ‘purple’));

A string object that can have 0 or more values, which is chosen from a **SET(a, b, c, etc )** list of values which you define, up to a maximum of 64 values. Think of 

SET being similar to HTML checkboxes in this regard.

**Numeric Data Types**

**Numeric Data Types**

**Data Type Description**

A bit-value type with a default of 1. The allowed number of bits in a **BIT(size)**

value is set via the size parameter, which can hold values from 1 to 64.

A very small integer with a signed range of -128 to 127, and an **TINYINT(size)** unsigned range of 0 to 255. Here, the size parameter specifies the 

maximum allowed display width, which is 255.

Essentially a quick way of setting the column to TINYINT with a size of **BOOL**

\1. 0 is considered false, whilst 1 is considered true.

**BOOLEAN** Same as BOOL.

A small integer with a signed range of -32768 to 32767, and an **SMALLINT(size)** unsigned range from 0 to 65535. Here, the size parameter specifies 

the maximum allowed display width, which is 255.

**Numeric Data Types**

**Data Type Description**

A medium integer with a signed range of -8388608 to 8388607, **MEDIUMINT(size)** and an unsigned range from 0 to 16777215. Here, the size parameter 

specifies the maximum allowed display width, which is 255.

A medium integer with a signed range of -2147483648 to 

2147483647, and an unsigned range from 0 to 4294967295. Here, the **INT(size)**

size parameter specifies the maximum allowed display width, which is 255.

**INTEGER(size)** Same as INT.

A medium integer with a signed range of -9223372036854775808 

to 9223372036854775807, and an unsigned range from 0 to **BIGINT(size)**

18446744073709551615. Here, the size parameter specifies the maximum allowed display width, which is 255.

A floating point number value. If the precision (p) parameter is between 

0 to 24, then the data type is set to FLOAT(), whilst if its from 25 to 53, **FLOAT(p)**

the data type is set to DOUBLE(). This behaviour is to make the storage of values more efficient.

A floating point number value where the total digits are set by the size **DOUBLE(size, d)** parameter, and the number of digits after the decimal point is set by 

the d parameter.

An exact fixed point number where the total number of digits is set by the size parameters, and the total number of digits after the decimal point is set by the d parameter.

**DECIMAL(size, d)**

For size, the maximum number is 65 and the default is 10, whilst for d, the maximum number is 30 and the default is 10.

**DEC(size, d)** Same as DECIMAL.

**Date / Time Data Types**

**Date / Time Data Types**

**Data Type Description**

A simple date in YYYY-MM DD format, with a supported range from **DATE**

` `1000-01-01  to  9999-12-31 .

A date time in YYYY-MM-DD hh:mm:ss format, with a supported range from  1000-01-01 00:00:00  to  9999-12-31 23:59:59 .

**DATETIME(fsp)**

By adding DEFAULT and ON UPDATE to the column definition, it automatically sets to the current date/time.

A Unix Timestamp, which is a value relative to the number of seconds 

since the Unix epoch ( 1970-01-01 00:00:00  UTC). This has a 

supported range from  1970-01-01 00:00:01  UTC to  2038-01-09 **TIMESTAMP(fsp)** 03:14:07  UTC.

By adding DEFAULT CURRENT\_TIMESTAMP and ON UPDATE CURRENT TIMESTAMP to the column definition, it automatically sets to current date/time.

A time in hh:mm:ss format, with a supported range from  -838:59:59  **TIME(fsp)** 

to  838:59:59 .

**YEAR** A year, with a supported range of  1901  to  2155 .

**Operators**

**Arithmetic Operators**

**Arithmetic Operators**

**Operator Description**

**+** Add Subtract

**\*** Multiply

**/** Divide **%** Modulo

**Bitwise Operator**

**Bitwise Operator**

**Operator Description**

**&** Bitwise AND

**|** Bitwise OR **^** Bitwise exclusive OR

**Comparison Operators**

**Comparison Operators**

**Operator Description**

**=** Equal to

**>** Greater than

**<** Less than

**>=** Greater than or equal to **<=** Less than or equal to **<>** Not equal to

**Compound Operators**

**Compound Operators Operator Description**

**+=** Add equals

**-=** Subtract equals

**\*=** Multiply equals

**/=** Divide equals

**%=** Modulo equals

**&=** Bitwise AND equals

**^-=** Bitwise exclusive equals

**|\*=** Bitwise OR equals

**Functions**

**Strin  Functions**

**Strin  Functions**

**Name Description**

**ASCII** Returns the equivalent ASCII value for a specific character. **CHAR\_LENGTH** Returns the character length of a string.

**CHARACTER\_**

Same as CHAR\_LENGTH. **LENGTH**

**CONCAT** Adds expressions together, with a minimum of 2.

**CONCAT\_WS** Adds expressions together, but with a separator between each value.

Returns an index value relative to the position of a value within a list of **FIELD**

values.

**FIND IN SET** Returns the position of a string in a list of strings.

When passed a number, returns that number formatted to include **FORMAT**

commas (eg 3,400,000).

Allows you to insert one string into another at a certain point, for a **INSERT**

certain number of characters.

**INSTR** Returns the position of the first time one string appears within another. **LCASE** Convert a string to lowercase.

Starting from the left, extract the given number of characters from a **LEFT**

string and return them as another.

**LENGTH** Returns the length of a string, but in bytes.

**LOCATE** Returns the first occurrence of one string within another, **LOWER** Same as LCASE.

**LPAD** Left pads one string with another, to a specific length. **LTRIM** Remove any leading spaces from the given string.

**Strin  Functions**

**Name Description**

**MID** Extracts one string from another, starting from any position.

Returns the position of the first time one substring appears within **POSITION**

another.

**REPEAT** Allows you to repeat a string

Allows you to replace any instances of a substring within a string, with **REPLACE**

a new substring.

**REVERSE** Reverses the string.

Starting from the right, extract the given number of characters from a **RIGHT**

string and return them as another.

**RPAD** Right pads one string with another, to a specific length. **RTRIM** Removes any trailing spaces from the given string.

**SPACE** Returns a string full of spaces equal to the amount you pass it. **STRCMP** Compares 2 strings for differences

**SUBSTR** Extracts one substring from another, starting from any position. **SUBSTRING** Same as SUBSTR

**SUBSTRING\_** Returns a substring from a string before the passed substring is found **INDEX** the number of times equals to the passed number.

Removes trailing and leading spaces from the given string. Same as if **TRIM**

you were to run LTRIM and RTRIM together.

**UCASE** Convert a string to uppercase. **UPPER** Same as UCASE.

**Numeric Functions**

**Numeric Functions**

**Name Description![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.016.png)**

**ABS** Returns the absolute value of the given number. **ACOS** Returns the arc cosine of the given number.

**ASIN** Returns the arc sine of the given number.

**ATAN** Returns the arc tangent of one or 2 given numbers. **ATAN2** Return the arc tangent of 2 given numbers.

**AVG** Returns the average value of the given expression.

Returns the closest whole number (integer) upwards from a given **CEIL**

decimal point number.

**CEILING** Same as CEIL.

**COS** Returns the cosine of a given number.

**COT** Returns the cotangent of a given number.

**COUNT** Returns the amount of records that are returned by a SELECT query. **DEGREES** Converts a radians value to degrees.

**DIV** Allows you to divide integers.

**EXP** Returns e to the power of the given number.

Returns the closest whole number (integer) downwards from a given **FLOOR**

decimal point number.

**GREATEST** Returns the highest value in a list of arguments. **LEAST** Returns the smallest value in a list of arguments. **LN** Returns the natural logarithm of the given number

Returns the natural logarithm of the given number, or the logarithm of **LOG**

the given number to the given base

**LOG10** Does the same as LOG, but to base 10.

**Numeric Functions**

**Name Description![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.017.png)**

**LOG2** Does the same as LOG, but to base 2.

**MAX** Returns the highest value from a set of values. **MIN** Returns the lowest value from a set of values.

Returns the remainder of the given number divided by the other given **MOD**

number.

**PI** Returns PI.

Returns the value of the given number raised to the power of the other **POW**

given number.

**POWER** Same as POW.

**RADIANS** Converts a degrees value to radians.

**RAND** Returns a random number.

**ROUND** Round the given number to the given amount of decimal places. **SIGN** Returns the sign of the given number.

**SIN** Returns the sine of the given number.

**SQRT** Returns the square root of the given number.

**SUM** Returns the value of the given set of values combined.

**TAN** Returns the tangent of the given number.

**TRUNCATE** Returns a number truncated to the given number of decimal places.

**Date Functions**

**Numeric Functions**

**Name Description**

Add a date interval (eg: 10 DAY) to a date (eg: 20/01/20) and return **ADDDATE**

the result (eg: 20/01/30).

Add a time interval (eg: 02:00) to a time or datetime (05:00) and **ADDTIME**

return the result (07:00).

**CURDATE** Get the current date. **CURRENT\_DATE** Same as CURDATE. **CURRENT\_TIME** Get the current time.

**CURRENT\_**

Get the current date and time. **TIMESTAMP**

**CURTIME** Same as CURRENT\_TIME.

**DATE** Extracts the date from a datetime expression. **DATEDIFF** Returns the number of days between the 2 given dates. **DATE\_ADD** Same as ADDDATE.

**DATE\_FORMAT** Formats the date to the given pattern.

Subtract a date interval (eg: 10 DAY) to a date (eg: 20/01/20) and **DATE\_SUB**

return the result (eg: 20/01/10).

**DAY** Returns the day for the given date.

**DAYNAME** Returns the weekday name for the given date.

**DAYOFWEEK** Returns the index for the weekday for the given date. **DAYOFYEAR** Returns the day of the year for the given date.

**EXTRACT** Extract from the date the given part (eg MONTH for 20/01/20 = 01). **FROM DAYS** Return the date from the given numeric date value.

**HOUR** Return the hour from the given date.

**Numeric Functions**

**Name Description![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.018.png)**

**LAST DAY** Get the last day of the month for the given date. **LOCALTIME** Gets the current local date and time. **LOCALTIMESTAMP** Same as LOCALTIME.

Creates a date and returns it, based on the given year and number of **MAKEDATE**

days values.

Creates a time and returns it, based on the given hour, minute and **MAKETIME**

second values.

**MICROSECOND** Returns the microsecond of a given time or datetime.

**MINUTE** Returns the minute of the given time or datetime.

**MONTH** Returns the month of the given date.

**MONTHNAME** Returns the name of the month of the given date.

**NOW** Same as LOCALTIME.

**PERIOD\_ADD** Adds the given number of months to the given period. **PERIOD\_DIFF** Returns the difference between 2 given periods.

**QUARTER** Returns the year quarter for the given date.

**SECOND** Returns the second of a given time or datetime. **SEC\_TO\_TIME** Returns a time based on the given seconds.

**STR\_TO\_DATE** Creates a date and returns it based on the given string and format. **SUBDATE** Same as DATE\_SUB.

Subtracts a time interval (eg: 02:00) to a time or datetime (05:00) **SUBTIME**

and return the result (03:00).

**SYSDATE** Same as LOCALTIME.

**TIME** Returns the time from a given time or datetime. **TIME\_FORMAT** Returns the given time in the given format.

**Numeric Functions**

**Name Description**

**TIME\_TO\_SEC** Converts and returns a time into seconds.

**TIMEDIFF** Returns the difference between 2 given time/datetime expressions. **TIMESTAMP** Returns the datetime value of the given date or datetime.

Returns the total number of days that have passed from  00-00- **TO\_DAYS**

0000  to the given date.

**WEEK** Returns the week number for the given date. **WEEKDAY** Returns the weekday number for the given date. **WEEKOFYEAR** Returns the week number for the given date.

**YEAR** Returns the year from the given date.

**YEARWEEK** Returns the year and week number for the given date.

**Misc Functions**

**Numeric Functions**

**Name Description![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.019.png)**

**IN** Returns the given number in binary.

**BINARY** Returns the given value as a binary string.

**CAST** Convert one type into another.

**COALESCE** From a list of values, return the first non-null value. **CONNECTION\_ID** For the current connection, return the unique connection ID.

Convert the given number from one numeric base system into **CONV**

another.

**CONVERT** Convert the given value into the given datatype or character set.

Return the user and hostname which was used to authenticate with **CURRENT\_USER**

the server.

**DATABASE** Get the name of the current database.

Used alongside aggregate functions (COUNT, MAX, MIN, SUM, AVG) to group the results.

**Example: Lists the number of users with active orders. GROUP BY**

SELECT COUNT(user\_id), active\_orders FROM users

GROUP BY active\_orders;

It s used in the place of WHERE with aggregate functions.

**Example: Lists the number of users with active orders, but only include users with more than 3 active orders.**

**HAVING**

SELECT COUNT(user\_id), active\_orders FROM users

GROUP BY active\_orders

HAVING COUNT(user\_id) > 3;

**IF** If the condition is true return a value, otherwise return another value. **IFNULL** If the given expression equates to null, return the given value.

**Numeric Functions**

**Name Description**

**ISNULL** If the expression is null, return 1, otherwise return 0.

For the last row which was added or updated in a table, return the **LAST\_INSERT\_ID**

auto increment ID.

Compares the 2 given expressions. If they are equal, NULL is returned, **NULLIF**

otherwise the first expression is returned.

**SESSION\_USER** Return the current user and hostnames.

**SYSTEM\_USER** Same as SESSION\_USER.

**USER** Same as SESSION\_USER.

**VERSION** Returns the current version of the MySQL powering the database.

**Wildcard Characters**

In SQL, Wildcards are special characters used with the LIKE and NOT LIKE keywords which allow us to search data with sophisticated patterns much more efficiently



|**Wildcards**|
| - |
|**Name**|**Description**|
|**%**|<p>Equates to zero or more characters. </p><p>**Example 1**:F ind all users with surnames ending in  son .</p><p>SELECT \* FROM users WHERE surname LIKE '%son';</p><p>**Example 2**:F ind all users living in cities containing the pattern  che SELECT \* FROM users</p><p>WHERE city LIKE '%che%';</p>|
|**\_**|<p>Equates to any single character.</p><p>**Example**:F ind all users living in cities beginning with any 3 characters, follow by  chester .</p><p>SELECT \* FROM users WHERE city LIKE '\_\_\_chester';</p>|
|**[charlist]**|<p>Equates to any single character in the list.</p><p>**Example 1:**F ind all users with first names beginning with J, H or M. SELECT \* FROM users</p><p>WHERE first\_name LIKE '[jhm]%';</p><p>**Example 2:**F ind all users with first names beginning letters between A L. SELECT \* FROM users</p><p>WHERE first\_name LIKE '[a-l]%';</p><p>**Example 3:**F ind all users with first names not ending with letters between n s. SELECT \* FROM users</p><p>WHERE first\_name LIKE '%[!n-s]';</p>|
**Keys**

In relational databases, there is a concept of primary and foreign keys. In SQL tables, these are included as constraints, where a table can have a primary key, a foreign key, or both.

**Primary Key**

A primary key allows each record in a table to be uniquely identified. There can only be one primary key per table, and you can assign this constraint to any single or combination of columns. However, this means each value within this column(s) must be unique.

Typically in a table, the primary key is an ID column, and is usually paired with the AUTO\_ INCREMENT keyword. This means the value increases automatically as new records are created.

**Example 1 (MySQL)**

Create a new table and set the primary key to the ID column.

CREATE TABLE users (

id int NOT NULL AUTO\_INCREMENT, first\_name varchar(255), last\_name varchar(255) NOT NULL, address varchar(255), email varchar(255),

PRIMARY KEY (id)

);

**Example 2 (MySQL)**

Alter an existing table and set the primary key to the first\_name column.

ALTER TABLE users

ADD PRIMARY KEY (first\_name);

**Forei n Key**

A foreign key can be  ![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.020.jpeg)applied to one column  

or many and is used to  link 2 tables together in a  relational database. 

As seen in the diagram  below, the table containing  the foreign key is called  the child key, whilst the  table which contains  

the referenced key, or  candidate key, is called the  parent table. 

This essentially means  that the column data is  shared between 2 tables,  as a foreign key also  prevents invalid data from  being inserted which isn t  also present in the parent  table. 

**Example 1 (MySQL)**

Create a new table and turn any columns that reference IDs in other tables into foreign keys.

CREATE TABLE orders (

id int NOT NULL,

user\_id int,

product\_id int,

PRIMARY KEY (id),

FOREIGN KEY (user\_id) REFERENCES users(id), FOREIGN KEY (product\_id) REFERENCES products(id) );

**Example 2 (MySQL)**

Alter an existing table and create a foreign key.

**ALTER** **TABLE** orders

**ADD** **FOREIGN** **KEY** (user\_id) **REFERENCES** users(id);

**Indexes**

Indexes are attributes that can be assigned to columns that are frequently searched against to make data retrieval a quicker and more efficient process.

This doesn t mean each column should be made into an index though, as it takes longer for a column with an index to be updated than a column without. This is because when indexed columns are updated, the index itself must also be updated.



|**Wildcards**|
| - |
|**Name**|**Description**|
|**CREATE INDEX**|<p>Creates an index named  idx\_test  on the first\_name and surname columns of the users table. In this instance, duplicate values are allowed.</p><p>**CREATE** **INDEX** idx\_test</p><p>**ON** users (first\_name, surname);</p>|
|**CREATE UNIQUE INDEX**|<p>Creates an index named  idx\_test  on the first\_name and surname columns of the users table. In this instance, duplicate values are allowed.</p><p>**CREATE** UNIQUE **INDEX** idx\_test **ON** users (first\_name, surname);</p>|
|**DROP INDEX**|<p>Creates an index named  idx\_test  on the first\_name and surname columns of the users table. In this instance, duplicate values are allowed.</p><p>**ALTER** **TABLE** users **DROP** **INDEX** idx\_test;</p>|
**Joins**

In SQL, a JOIN clause is used to return a results set which combines data from multiple tables, based on a common column which is featured in both of them

There are a number of different joins available for you to use:

Inner Join (Default): Returns any records which have matching values in both tables.

Left Join: Returns all of the records from the first table, along with any matching records from the second table.

Right Join: Returns all of the records from the second table, along with any matching records from the first.

Full Join: Returns all records from both tables when there is a match. A common way of visualising how joins work is like this:

**INNER JOIN LEFT JOIN RIGHT JOIN OUTER JOIN        Table 1 Table 2 Table 1 Table 2 Table 1 Table 2 Table 1 Table 2![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.021.png)![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.022.png)![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.023.png)![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.024.png)**

In the following example, ![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.025.jpeg)an inner join will be used to create a new unifying view combining the orders table and then 3 different tables

We ll replace the user\_id and product\_id with the first\_name and surname columns of the user who placed the order, along with the name of the item which was purchased.

**SELECT** orders.id, users.first\_name, users.surname, products.name **as** ‘product name’ **FROM** orders

**INNER** **JOIN** users **on** orders.user\_id = users.id

**INNER** **JOIN** products **on** orders.product\_id = products.id;

Would return a results set which looks like:

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.026.jpeg)

**View**

A view is essentially a SQL results set that get stored in the database under a label, so you can return to it later, without having to rerun the query. These are especially useful when you have a costly SQL query which may be needed a number of times, so instead of running it over and over to generate the same results set, you can just do it once and save it as a view.

**Creatin  Views**

To create a view, you can do so like this:

**CREATE** **VIEW** priority\_users **AS ![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.027.png)**

**SELECT** \* **FROM** users 

**WHERE** country = ‘United Kingdom’; 

Then in future, if you need to access the stored result set, you can do so like this: 

**SELECT** \* **FROM** [priority\_users]; 

**Replacin  Views** 

With the CREATE OR REPLACE command, a view can be updated. 

**CREATE** OR **REPLACE** **VIEW** [priority\_users] **AS** 

**SELECT** \* **FROM** users 

**WHERE** country = ‘United Kingdom’ OR country=’USA’; 

**Deletin  Views** 

To delete a view, simply use the DROP VIEW command. 

**DROP** **VIEW** priority\_users; 

**Conclusions![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.028.png)**

The majority of the websites on today s web use relational databases in some way. This makes SQL a valuable language to know, as it allows you to create more complex, functional websites and systems.

Make sure to bookmark this page, so in the future, if you re working with SQL and can t quite remember a specific operator, how to write a certain query, or are just confused about how joins work, then you ll have a cheat sheet on hand which is ready, willing and able to help.

![](Aspose.Words.6294defc-0a0f-444a-b8e1-65836eff5024.029.png)
