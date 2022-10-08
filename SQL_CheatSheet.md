
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
  
	#List available tables
		show tables;

	#List field names and settings etc
		describe "table name";

	#List all contents of the selected table
		select * from "table name";

	#Insert contents into table
		insert into "table name" ( , , , , ) values ( , , , , );
			Tip: The table rows will need to be added after the table name and then the values you would like to insert after values.

	#Update specified row by specifying id of row
		update "table name" set "column name" = "data in row", where "column name" = "data in row"

	#Viewing tables in the selected database
	   show tables;

	#Renaming of a table
	   rename table "table name" to "table name2";
	   alter table "table name" rename to "table name2;

    #Adding a column
	   alter table "table name" add column "column name" real;

	#Dropping a column
	   alter table "table name" drop column "column name";

    #Create a view
       create view personal_info as select first_name, last_name, age from student;

    #Displaying view
       select * from personal_info;

    #Updating in view
       update personal_info set salary = 1.1 * salary;

    #Deleting record from view
       delete from personal_info where age < 40;
    
	#Droping a view
       drop view personal_info;

    #Functions
    #Sum function
       select sum(population) from city group by population;

    #Average function
       select avg(population) from city group by population;

    #Count function
       select district, count(district) from city group by district;

    #Maximum function
       select max(population) from city group by population;

    #Minimum function
       select min(population) from city group by population;

	  

	
    
    
