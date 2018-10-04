# WEB2040_data_generation_exercise
Practice how to create tables and populate them with randomly generated data

## Create the following database tables
Replace string by either CHAT, TEXT or ENUM as you beleive necesary. You can use phpMyAdmin or other mysql graphic tools to make your work easier.

```
inventory
----
id, int PK AUTOINCREMENT
product_name, string
category, string # office,home,garden,toys,cloths,shoes,cosmetics,other
vendor, int FK >- vendor
cost, float

vendor
---
id, int PK AUTOINCREMENT
name, string
phone, string
email, string
website, string
address, string
country, string(2) # 2 digits country code

sales
---
id, int PK AUTOINCREMENT
product, int FK >- inventory
customer, int FK >- customer
sold_time, datetime
amount, float
tax, float
shipping, float
deliver_address, string
deliver_zipcode, string
status, string # purchased, delivered, in_transit, returned

customer
---
id, int PK AUTOINCREMENT
name, string
phone, string
email, string
address, string
country, string(2)
```

## Fill the tables with random data
Download the SQL scheema (all tables in SQL language) and use the online tool http://filldb.info to fill the columns with randomly generated data. Create at least 5000 rows for the table "sales". Export the resulting SQL into your database. 

## Run the following reports
* Get the net total that the store earned on sales (items purchased - returns) 
* Get all products on your inventory that have never beign sold
* Get the customer name, product name and delivery address for all opened orders from Forida
