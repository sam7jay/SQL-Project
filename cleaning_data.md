What issues will you address by cleaning the data?

Removing the columns that only have null values
Removing columns containing duplicate data
Adjusting prices





Queries:
Below, provide the SQL queries you used to clean your data.

Remove unneccessary columns that only have null values
ALTER TABLE all_sessions DROP COLUMN itemrevenue;
Remove columns with duplicate data
ALTER TABLE all_sessions DROP COLUMN transactionrevenue;

Adjusting prices:

UPDATE all_sessions
 SET totaltransactionrevenue = totaltransactionrevenue/1000000
 WHERE totaltransactionrevenue IS NOT NULL;
 
