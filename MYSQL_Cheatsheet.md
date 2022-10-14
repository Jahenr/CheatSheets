MYSQL
        
        #Creates a new database if it does not exist.
                 CREATE DATABASE DATABASENAME;
    
        #Allow you to use a particular database or change from the current database to another database.
                 USE DATABASENAME;
    
        #Creates a new table in the current database.
                 CREATE TABLE TABLENAME (
                  COLUMN1 DATATYPE,
                  COLUMN2 DATATYPE,
                  COLUMN3 DATATYPE,
                  ....
                  CONSTRAINTS ....
                   );
       #Drop Table
                 DROP TABLE table_name;

	     #Add a new column into a table
		             ALTER TABLE TABLENAME ADD COLUMNNAME DATATYPE;

	     #Drop a column from a table
		             ALTER TABLE TABLENAME DROP COLUMN COLUMNNAME;

	#Displays all the rows of the cartesian product of the two tables
		SELECT * FROM TABLENAME1,TABLENAME2;

	#Select particular columns from table(s)
		SELECT COLUMN1,COLUMN2 FROM TABLENAME;

	#Displays rows based on negation of a particular condition
		SELECT * FROM TABLENAME WHERE NOT CONDITION

	#Used to sort results in ascending order or descending order
		SELECT … FROM TABLENAME ORDER BY COLUMN1 ASC|DESC;

	#Used to search for a specific pattern.
		SELECT COLUMN1 FROM TABLENAME WHERE COLUMN1 LIKE ‘%PATTERN%’;

	#Tests for existence of a certain record. Returns a boolean value.
		SELECT * FROM TABLE NAME WHERE EXIST (SUB QUERY);

	#Inner Join selects records that have the same values in two same or distinct tables.
		SELECT COLUMN(S) FROM TABLENAME1 INNER JOIN TABLENAME2 ON TABLENAME1.COLUMNAME=TABLENAME2.COLUMNAME;

	#Left Join selects all the records from the left table and matching records from the right table.
		SELECT COLUMN(S) FROM TABLENAME1 LEFT JOIN TABLENAME2 ON TABLENAME1.COLUMNAME=TABLENAME2.COLUMNAME;

	#Right Join selects all the records from the right table and matching records from the left table.
		SELECT COLUMN(S) FROM TABLENAME1 RIGHT JOIN TABLENAME2 ON TABLENAME1.COLUMNAME=TABLENAME2.COLUMNAME;

	#Union combines the result of two select statements.
		SELECT * FROM TABLENAME1 UNION SELECT * FROM TABLENAME2

	#Concat combines two or more columns together.
		SELECT CONCAT(COLUMN1, " ", POSTALCODE, " ", COLUMN2) AS NEWCOL FROM TABLENAME;

	#Create Index
		CREATE INDEX indexname ON tablename (column1, column2, ...);

	#Drop Index deletes an existing index.
		DROP INDEX INDEXNAME;

	#Creates a view if it doesn’t exist.
		CREATE VIEW VIEWNAME AS SELECT COLUMN1,COLUMN2 FROM TABLE WHERE CONDITION;

	#Creates or edits an existing view.
		CREATE OR REPLACE viewname AS SELECT COLUMN1,COLUMN2 FROM TABLE WHERE CONDITION;

	#Changes the name of the view.
		RENAME TABLE VIEWNAME TO NEWVIEWNAME;

	#Drop view
		DROP VIEW VIEWNAME;

	#Deletes multiple views.
		DROP VIEW VIEW1,VIEW2…;
