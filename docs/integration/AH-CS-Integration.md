# Integration


## Connect to Database

``` python
# Get extra code
import sqlite3

# Create a connection to a database
# Creates a new database file, if it doesn’t exist
connection = sqlite3.connect('example.db')

# Create a database cursor
cursor = connection.cursor()

#
# SQL goes here
#

# Close the connection to the database
connection.close()
```


## Create a Table

```python
# Create a table in the database.

# SQL to create a table - if it does not exist
new_table = '''
CREATE TABLE IF NOT EXISTS Manufacturer (
    manufacturerID INTEGER NOT NULL,
    name VARCHAR(20),
    address VARCHAR(40),
    telephone VARCHAR(11) 
        CHECK (LENGTH(telephone) = 11),
    PRIMARY KEY (manufacturerID)
);
'''

# Create the new table
cursor.execute(new_table)
```


## Insert Data

``` python
new_data = '''
INSERT INTO Manufacturer
    VALUES
        (441,'Craft Supplies','Wishaw Industrial Estate','01415437212'),
        (531,'Metal and Wood','Tyne Way Newcastle','01542123485'),
        (627,'Tool Makers','231 London Walk Bristol','01347234987');
'''

# Insert new data
cursor.execute(new_data)

# Commit the new data
conn.commit()
```


## Delete Data

``` python
# SQL to delete data
delete_data = '''
DELETE FROM Manufacturer
    WHERE name LIKE "%and%";
'''

# Run query to delete the data
cursor.execute(delete_data)
```


## Query the Database

``` python
query = '''
SELECT *
    FROM Manufacturer;
'''

# Run query and store result
result = cursor.execute(query)

# Display each row
for row in result:
    
    # Display row
    print(row)
```


## Drop a Table

``` python
# SQL to drop a table - if it exists
drop_table = '''
DROP TABLE IF EXISTS Manufacturer;
'''

# Run query to delete the data
cursor.execute(drop_table)
```