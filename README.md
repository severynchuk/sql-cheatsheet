# SQL Cheatsheet

## Database Schema

![Database Schema](/images/database_schema.jpg)

### transactions

| Column            | Data_Type | Constraint | Description      |
|-------------------|-----------|------------|------------------|
| id                | integer   | not null   | transaction ID   |
| transaction_type  | enum      | not null   | purchase/sale    |
| contractor_id     | integer   | not null   | contractor ID    |
| stock_id          | integer   | not null   | stock ID         |
| product_id        | integer   | not null   | produkt ID       |
| product_quantity  | numeric   | not null   | product quantity |
| product_price     | numeric   | not null   | product price    |

### contractors

| column | data_type | constraint | description        |
|--------|-----------|------------|--------------------|
| id     | integer   | not null   | contractor's ID    |
| name   | varchar   | not null   | contractor's name  |
| phone  | integer   | not null   | contractor's phone |
| city   | varchar   | not null   | contractor's city  |

### products

| column        | data_type | constraint | description                               |
| ------------- | --------- | ---------- | ----------------------------------------- |
| id            | integer   | not null   | product ID                                |
| name          | varchar   | not null   | product's name                            |
| unit          | enum      | not null   | unit of measure for the quantity of goods |
| cross_section | varchar   | not null   | wire cross-sectional area                 |

### stock

| column           | data_type | constraint | description      |
| ---------------- | --------- | ---------- | ---------------- |
| id               | integer   | not null   | stock ID         |
| product_id       | integer   | not null   | product ID       |
| manufacturer_id  | integer   | not null   | manufacturer ID  |
| product_quantity | varchar   | not null   | product quantity |

### manufacturers

| column | data_type | constraint | description          |
|--------|-----------|------------|----------------------|
| id     | integer   | not null   | manufacturers ID     |
| name   | varchar   | not null   | manufacturer's name  |
| phone  | integer   | not null   | manufacturer's phone |
| city   | varchar   | not null   | manufacturer's city  |
