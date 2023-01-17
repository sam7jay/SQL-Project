##What issues will you address by cleaning the data?

Removing the columns that only have null values
Removing columns containing duplicate data
Adjusting prices





##Queries:
Below, provide the SQL queries you used to clean your data.

###Remove unneccessary columns that only have null values
```SQL
ALTER TABLE all_sessions DROP COLUMN transactionrevenue;
```
###Remove columns with duplicate data
```SQL
ALTER TABLE all_sessions DROP COLUMN transactionrevenue;
```
###Adjusting prices:
```SQL
UPDATE all_sessions
 SET totaltransactionrevenue = totaltransactionrevenue/1000000
 WHERE totaltransactionrevenue IS NOT NULL;
 ```
