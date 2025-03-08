# Snowflake-project

start with create SQL worksheet,

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

---

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


