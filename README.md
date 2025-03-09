# Snowflake-project

- ini adalah (setting-up warehouse)[##Setting up Warehouse]

## start with create SQL worksheet,

<image src="https://github.com/user-attachments/assets/f4600b99-40e5-456a-8180-d9935292159c" width=30% heigh=30% />

then rename worksheet name into "Our first worksheet" name

<image src="https://github.com/user-attachments/assets/1c33c4a8-df25-43ea-8182-68e50f3db99d" width=30% heigh=30% />

from Database tab, 

![image](https://github.com/user-attachments/assets/fde48b1b-760b-49d1-82b1-e6ad34f5b985)

```sql
SELECT * FROM

-- Create a database from the share.
create database snowflake_sample_data from share sfc_samples.sample_data;

-- Grant the PUBLIC role access to the database.
-- Optionally change the role name to restrict access to a subset of users.
grant imported privileges on database snowflake_sample_data to role public;
```

to see table that we will used, click on snowflake_sample_data, then click TPCH-SF1, scroldown to Tables, 
at the CUSTOMER click on 3 dor then choos Place name in editor

![image](https://github.com/user-attachments/assets/beb27fce-b4cf-4e34-a42f-63e95e7c6c08)

the table name automatically placed on query editor

```sql
SELECT * FROM

SNOWFLAKE_SAMPLE_DATA.TPCH_SF1.CUSTOMER
```

the result are 

![image](https://github.com/user-attachments/assets/07e219ef-9a27-47eb-b062-28bee539a72b)

## Navigating Worksheets

we notice here that, there is a statement "No Database selected"

![image](https://github.com/user-attachments/assets/8e324a4e-30b9-4d05-8287-2a12d63db3df)

this happen because, we use fully qualified table name

![image](https://github.com/user-attachments/assets/0c83c81b-f905-48ea-912d-94202a1628e9)

this table name consist of 

SNOWFLAKE_SAMPLE_DATA : name of database

TPCH_SF1 : name of schema

CUSTOMER : name of table

if we remove database and schema name , like this

![image](https://github.com/user-attachments/assets/9c9a2aea-8022-49a1-b0a7-11f92239447d)

there would be an error, if we run this query

<image src="https://github.com/user-attachments/assets/33ffcf17-f9d8-4595-808c-a8b4291b09bb" width=60% heigh=60% />

we have to set an appropriate context, we can do this by click on "No Database selected" , 

then choose database name that is SNOWFLAKE_SAMPLE_DATA and choose schema name that is TPCH_SF1

![image](https://github.com/user-attachments/assets/9f334683-87c0-4351-afe8-26a85e2f9ad4)

the tag "No Database selected" changed to name of database + name of schema

![image](https://github.com/user-attachments/assets/3c6bbbe0-52da-49b4-b1dd-a4b0dccbdff4)

now we can run the query normally

in the top right corner there is our role 

![image](https://github.com/user-attachments/assets/953f2e8c-7339-4440-93bc-06b01b90d6a3)

as default, our role is as ACCOUNTADMIN

![image](https://github.com/user-attachments/assets/95a32eb1-2280-4342-8b39-f63094df985f)

we can change our role by click on other role, 

Sometimes the resulting table will be different, depending on the settings made by the accoun admin.

### Create Folder

click on Worksheet , then click plus sign , then click folder

![image](https://github.com/user-attachments/assets/27752e6c-3fc5-4ebe-af1f-8bb92a431d92)

we can name it with "First Folder"

![image](https://github.com/user-attachments/assets/62ae6374-47d4-4b26-b1bb-c6e535e1ec90)

now we go to Worksheet menu, then click Ou first worksheet

![image](https://github.com/user-attachments/assets/ecc7c688-36e5-4c86-b84d-6dc66dc89fa4)

now on the worksheet menu, we can see our new folder

![image](https://github.com/user-attachments/assets/1c58599e-5dac-41d6-a2d1-06dad535d5c2)

we then click on three dot beside our first worksheet, then click move, click on first folder

![image](https://github.com/user-attachments/assets/fd002884-0e38-45f8-a41c-5b89f92895fe)

now our first worksheet have moved to First folder

![image](https://github.com/user-attachments/assets/72561c48-d0d8-45f6-8bcc-95b0429d2297)


---
## Setting up Warehouse 




