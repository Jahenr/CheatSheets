
MariaDB:

	#Create user with password
		CREATE USER "username" IDENTIFIED BY "password";
	
	#Display users
		SELECT * FROM mysql.user;

	#List available databases
		SHOW databases;
		
	#Show tables from databases
		SHOW TABLES FROM database_name;

	#Create database
		CREATE DATABASE database_name";
  
	#Change to specified database
		USE database_name;
  
	#List available tables
		SHOW tables;

	#List field names and settings etc
		DESCRIBE table_name;

	#List all contents of the selected table
		SELECT * FROM table_name;

	#Insert contents into table
		INSERT INTO table_name ( , , , , ) VALUES ( , , , , );
			Tip: The table rows will need to be added after the table name and then the values you would like to insert after values.

	#Update specified row by specifying id of row
		UPDATE table_name
		SET column_name = "data in row"
		WHERE column_name = "data in row";
	
	#Disable foreign key checks
	         SET FOREIGN_KEY_CHECKS=0
        
	#Enable foreign key checks
	         SET FOREIGN_KEY_CHECKS=1
		 
	#Return the intersection of two queries
	         SELECT c1,c2 FROM t1
		 INTERSECT
		 SELECT c1,c2 FROM t2;
		 
	#Return the intersection of two queries
	         SELECT c1,c2 FROM t1
		 UNION
		 SELECT c1,c2 FROM t2;	 

	#Drop a table
		DROP TABLE [IF EXISTS] table_name;
		
	#Truncate a table
		TRUNCATE TABLE table_name;
		
	#Delete a table
		DELETE FROM table_name
		WHERE condition;
		
	#Dislay table
		TABLE table_name;
		
	#Grant
		GRANT privilage_name ON object_name TO "user@host";
		
	#Revoke
		REVOKE privilage_name ON object_name FROM "user@host";
		
	#Rename table
		RENAME TABLE table_name TO table_name;
		
		
		
		

	
    
    
