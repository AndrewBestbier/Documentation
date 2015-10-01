##Select Statements:

###The SELECT statement is used to select data from a database:

~~~ sql
SELECT * FROM table_name;
~~~

or

~~~ sql
SELECT column_name,column_name
FROM table_name;
~~~

###The DISTINCT keyword can be used to return only distinct values:

~~~ sql
SELECT DISTINCT column_name,column_name
FROM table_name;
~~~

###The WHERE clause is used to extract only those records that fulfill a specified criterion:
~~~ sql
SELECT column_name,column_name
FROM table_name
WHERE column_name operator value;
~~~
* Single quotes around text values
* <> Not equal


#####And Or operators:
~~~ sql
SELECT * FROM Customers
WHERE Country='Germany'
AND/OR City='Berlin';
~~~


###The ORDER BY keyword is used to sort the result-set by one or more columns:
~~~ sql
SELECT column_name, column_name
FROM table_name
ORDER BY column_name ASC|DESC, column_name ASC|DESC;
~~~
* Order by Asc is default
* Yes you can order by separate columns. Ordered sequentially

###The LIKE operator is used to search for a specified pattern in a column.

~~~ sql
SELECT column_name(s)
FROM table_name
WHERE column_name LIKE pattern;
~~~


##Modifing table values:

###Inserting new values:
You can insert values into tables in the following two ways:

~~~ sql
INSERT INTO table_name
VALUES (value1,value2,value3,...);
~~~
The second form specifies both the column names and the values to be inserted:

~~~ sql
INSERT INTO table_name (column1,column2,column3,...)
VALUES (value1,value2,value3,...);
~~~
###Updating existing values:
~~~ sql
UPDATE table_name
SET column1=value1,column2=value2,...
WHERE some_column=some_value;
~~~
###Deleting existing values:
~~~ sql
DELETE FROM table_name
WHERE some_column=some_value;
~~~


