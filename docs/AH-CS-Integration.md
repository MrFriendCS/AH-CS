# Integration


## Notes

All the code examples use Python.

These notes are focused on Advanced Higher Computing Science so some terms are used differently.


## Database


### Connect to Database

``` python
# Get extra code
import sqlite3

# Create a connection to a database
# Creates a new database file, if it doesn’t exist
conn = sqlite3.connect('example.db')

# Create a database cursor
cursor = conn.cursor()

#
# SQL goes here
#

# Close the connection to the database
conn.close()
```


### Create a Table

```python
# Create a table in the database.

# SQL to create a table - if it does not exist
newTable = """
CREATE TABLE IF NOT EXISTS Manufacturer (
    manufacturerID INT NOT NULL,
    name VARCHAR(20),
    address VARCHAR(40),
    telephone VARCHAR(11) 
        CHECK (LENGTH(telephone) = 11),
    PRIMARY KEY (manufacturerID)
);
"""

# Create the new table
cursor.execute(newTable)
```


### Insert Data

``` python
newData = """
INSERT INTO Manufacturer
    VALUES
        (441,"Craft Supplies","Wishaw Industrial Estate","01415437212"),
        (531,"Metal and Wood","Tyne Way Newcastle","01542123485"),
        (627,"Tool Makers","231 London Walk Bristol","01347234987");
"""

# Insert new data
cursor.execute(newData)

# Commit the new data
conn.commit()
```


### Delete Data

``` python
# SQL to delete data
deleteData = """
DELETE FROM Manufacturer
    WHERE name LIKE "%and%";
"""

# Run query to delete the data
cursor.execute(deleteData)
```


### Query the Database

``` python
query = """
SELECT *
    FROM Manufacturer;
"""

# Run query and store result
result = cursor.execute(query)

# Dislay all rows
for row in result:
    
    # Display row
    print(row)
```
