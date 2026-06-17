# Database Design and Development


## Notes

All the code examples use SQLite.
They will work with [DB Browser for SQLite](https://sqlitebrowser.org/).


## Auto Increment

Auto increment can be used to automatically generate values for a field, normally the primary key.
When a record is added to a table the value for the primary key is omitted and the 


### Create a table

``` sql
CREATE TABLE IF NOT EXISTS Person (
    test_id INTEGER NOT NULL,
    name VARCHAR(20),
    age INTEGER
        CHECK (age >= 0),
    height REAL
        CHECK (height >= 0.3),
    PRIMARY KEY (test_id AUTOINCREMENT)
);
```


### Insert Data

``` sql
INSERT INTO Person (name, age, height)
    VALUES ("Sam", 5, 1.23);
    

INSERT INTO Person (name, age, height)
    VALUES ("Beth", 13, 1.65),
           ("Ivy", 9, 1.42);
```


### Select Data

``` sql
SELECT *
    FROM Test;
```


#### Output

| test_id | name | age  | height |
| ------- | ---- | ---- | ------ |
| 1       | Alan | 5    | 1.23 |
| 2       | Beth | 13   | 1.65 |
| 3       | Ivy  | 9    | 1.42 |
