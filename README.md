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
