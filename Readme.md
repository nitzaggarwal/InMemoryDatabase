
# INMEMORY-DATABASE

This is a Simple Inmemory Database application using Python which can be used as non-persistent in-memory database storage during execution of any application

# This code demonstrates the following functional Capabilities:
## Instructions to run the application

#### Run the app.py file to run the predefined instructions OR create another Database Manager Object to run custom instructions.
```
run app.py
```
Or create a new Database Manager for custom instructions
```
app = DatabaseManager()

```
### creating a database.
create a Database *db1* into app and pass a Database name
```
db1 = app.createDatabase("Verizon")
```

### selecting a particular Database from a Database Manager
get a Database Verizon from app. returns the Database object if it exists. 

```
verizonDB = app.getDatabase("Verizon")
```
### Creating Tables in a particular Database
create a table into a database. Pass table name and coloumn attributes \ 
Attributes Format [("coloumn 1 name","String"),("coloumn 2 name","String/Number"),("coloumn 3 name","Number/String"),("coloumn 4 name","Number/String")]

```
employeeTable = verizonDB.createTable("Employee",[("user_name","String"),("address","String"),("phone","Number")])
```

### Dropping a particular Table
```
VerizonDB.dropTable("Employee")
```

### selecting a Table
select an exisiting table, returns an object of table
```  
table1 = VerizonDB.selectTable("Employee")    
```

### Inserting rows in a Table

Inserts a row in a selected table

```
table1.insert([("user_name","Abc"),("address","33rd South"),("phone",32323212365)])
```

### Updating rows in a Table
This updates an exisiting record from a selected table

```
table1.update(1,{"user_name":"Swapnil","address":"33rd South","phone":232232})    
```
### Deleting a row from a Table
Delete a specific row from the selected table
```
 table1.delete(2)
```
### get specific row from a Table
get specific rows from a selected table returns a list of rows
```
table1.get_rows(2)
```
### SORT BY rows with a coloumn parameter in Ascending or Descending order
This sorts the rows of the table with reference to specific coloumn parameter that is passed. Returns a list of rows in sorted order
specify Coloumn name and 'asc' for Ascending / 'dsc' for Descending order
```
table1.order_by("user_name","asc")
```
### GroupBY rows with reference to a coloumn parameter. Returns count 

This groups the rows with reference to the specified coloumn name, and returns a list of different values and their counts . 

```
table1.group_by("address"))
```


