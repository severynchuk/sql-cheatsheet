# SQL Cheatsheet

## Database Schema

![Database Schema](/images/database_schema.png)

### transactions

| Column            | Data_Type | Constraint | Description      |
|-------------------|-----------|------------|------------------|
| id                | integer   | not null   | transaction ID   |
| transaction_type  | enum      | not null   | purchase/sale    |
| contractor_id     | integer   | not null   | contractor ID    |
| stock_id          | integer   | not null   | stock ID         |
| product_id        | integer   | not null   | product ID       |
| product_quantity  | double    | not null   | product quantity |
| product_price     | double    | not null   | product price    |

### contractors

| Column | Data_Type | Constraint | Description        |
|--------|-----------|------------|--------------------|
| id     | integer   | not null   | contractor ID      |
| name   | varchar   | not null   | contractor name    |
| phone  | varchar   | not null   | contractor phone   |
| city   | varchar   | not null   | contractor city    |

### products

| Column        | Data_Type | Constraint | Description                               |
| ------------- | --------- | ---------- | ----------------------------------------- |
| id            | integer   | not null   | product ID                                |
| name          | varchar   | not null   | product name                              |
| unit          | enum      | not null   | unit of measure for the quantity of goods |
| cross_section | double    | not null   | wire cross-sectional area                 |

### stock

| Column           | Data_Type | Constraint | Description      |
| ---------------- | --------- | ---------- | ---------------- |
| id               | integer   | not null   | stock ID         |
| product_id       | integer   | not null   | product ID       |
| manufacturer_id  | integer   | not null   | manufacturer ID  |
| product_quantity | double    | not null   | product quantity |

### manufacturers

| Column | Data_Type | Constraint | Description          |
|--------|-----------|------------|----------------------|
| id     | integer   | not null   | manufacturers ID     |
| name   | varchar   | not null   | manufacturer name    |
| phone  | varchar   | not null   | manufacturer phone   |
| city   | varchar   | not null   | manufacturer city    |
