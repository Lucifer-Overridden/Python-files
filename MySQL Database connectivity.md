# MySQL connectivity in Python 

## Install MySQL driver 

* Python needs a MySQL driver to access the MySQL database and here we are using **MySQL Connector** which can be installed by sing the command given below on your PIP terminal

``` bash
python3 -m pip install mysql-connector
```
* PIP is most likely installed in you python environment 

## Test MySQL connector

Now we need to test if the **MySQL connector** that we installed using PIP is working fine and to do that we need to test it in our python environment

``` Python
import mysql.connector
```
If the above code is executed with 0 errors then **MySQL connector** is installed and ready to be used.

## Creating connection

* Now we will create the connection between **Python** and **MySQL**
* Use the *username* and *password* from your SQL database

```Python
import mysql.connector

mydb = mysql.connector.connect(
  host = 'localhost',
  user = 'yourusername',
  password = 'yourpassword'
 )
 
 print(mydb)
 ```
 * If this file gives output similar to given below then you can move on to the next step
 
 ``` bash
 <mysql.connector.connection.MySQLConnection object at 0x1045e49470>
 ```
## Creating a database

* To create a database in **MySQL** we use the **'create database'** statement

```Python
import mysql.connector

mydb = mysql.connector.connect(
  host = 'localhost',
  user = 'yourusername',
  password = 'yourpassword'
 )
 
 mycursor = mydb.cursor()
 
 mycursor.execute("Create database mydatabase")
 ```
 * If the above code is executed with no errors then you have successfully created a database

## Check if database exists

* We check the existing databases by listing all the databases in our system by ising **'Show Databases'** command

```Python
import mysql.connector

mydb = mysql.connector.connect(
  host = 'localhost',
  user = 'yourusername',
  password = 'yourpassword'
 )

mycursor = mydb.cursor()

mycursor.execute('Show Databases')

for x in mycursor:
    print(x)
```
OR
* You can access the database while establishing the connection :

```Python
import mysql.connector

mydb = mysql.connector.connect(
  host = 'localhost',
  user = 'yourusername',
  password = 'yourpassword',
  database = 'youtdatabase'
 )
 ```
 * If the database does not exist then you will get an error 

## Creating a Table

* To create a table in **SQL** we use **'Create Table** command 

``` Python
import mysql.connector 

mydb = mysql.connector.connect(
    host = 'localhost',
    user =' yourusername',
    password = 'yourpassword',
    database = 'yourdatabase'
)

mycursor = mydb.cursor()

mycursor.execute("Create table customers (name varchar(100), address varchar(100)")

```

* If the code is executed with 0 errors that means you have successfully created the table

## Check if a table exists

* you can check if a table exists by listing all the tables present in the database

``` Python
import mysql.connector 

mydb = mysql.connector.connect(
    host = 'localhost',
    user =' yourusername',
    password = 'yourpassword',
    database = 'yourdatabase'
)

mycursor = mydb.cursor()

mycursor.execute("Show tables")

for x in mycursor :
    print(x)

```
## Primary Key

* When creating a table, you should also create a column with a unique key for each record which can be done by defining a **PRIMARY KEY** 
* The features of primary key column are that values in it can't be repeated and no cell can be null
* We can use the statement *"INT AUTO_INCREMENT PRIMARY KEY"* which will insert a unique number for each record, starting at 1 and incrementinh by 1 with each record

``` Python
import mysql.connector 

mydb = mysql.connector.connect(
    host = 'localhost',
    user =' yourusername',
    password = 'yourpassword',
    database = 'yourdatabase'
)

mycursor = mydb.cursor()

mycursor.execute("Create Table customers(id INT AUTO_INCREMENT PRIMARY KEY, name varchar(100), address varchar(100)")

```

## Insert into Table

* To fill a table in MySQL, we can use "INSERT INTO" statement

``` Python
import mysql.connector 

mydb = mysql.connector.connect(
    host = 'localhost',
    user =' yourusername',
    password = 'yourpassword',
    database = 'yourdatabase'
)

mycursor = mydb.cursor()

sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"
val = ("John", "Highway 21")

mydb.commit()

print(mycursor.rowcount, "record inserted")

```
