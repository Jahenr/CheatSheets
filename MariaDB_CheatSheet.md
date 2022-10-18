
MariaDB:

	#Create user with password
		create user "username" identified by "password";
	
	#Display users
		select * from mysql.user;

	#List available databases
		show databases;

	#Create database
		create database "database name";
  
	#Change to specified database
		use "database name";

	#Create table
		CREATE TABLE [IF NOT EXISTS] "table name" ("field name" "field type");

	#List available tables
		show tables;

	#List field names and settings etc
		describe "table name";

	#List all contents of the selected table
		select * from "table name";

	#Insert contents into table
		insert into "table name" ( , , , , ) values ( , , , , );
			Tip: The table rows will need to be added after the table name and then the values you would like to insert after values.

	#Insert new field to table
		ALTER TABLE "table name" ADD [COLUMN] "field name" "field type" [NOT NULL];

	#Update specified row by specifying id of row
		update "table name" set "column name" = "data in row", where "column name" = "data in row"
	
	#Disable foreign key checks
	         SET FOREIGN_KEY_CHECKS=0
        
	#Enable foreign key checks
	         SET FOREIGN_KEY_CHECKS=1
	 
	#DELETE it is used to remove one or more row from a table
	         DELETE FROM table_name [WHERE condition];

	#Return the intersection of two queries
	         SELECT c1,c2 FROM t1 INTERSECT SELECT c1,c2 FROM t2;

	#Drop a table
		DROP TABLE [IF EXISTS] table_name;

	#Drop column from table
		ALTER TABLE "table name" DROP [COLUMN] "field name";

	#Drop rows from table by applying specific condition/s
		DELETE FROM "table name" [WHERE "condition"];

	#Modify existing table field
		ALTER TABLE "table name" MODIFY [COLUMN] "field name" "field type" [NOT NULL];