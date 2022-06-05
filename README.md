# SQL Cheatsheet

## Database Schema

![Database Schema](/images/database_schema.jpg)

### transactions

| column            | data_type | constraint | description      |
|-------------------|-----------|------------|------------------|
| id                | integer   | not null   | transaction id   |
| type_transactions | varchar   | not null   | purchase/sale    |
| id_kontragenta    | integer   | not null   | kontragent id    |
| id_stock          | integer   | not null   | stock id         |
| id_produkt        | integer   | not null   | produkt id       |
| product quantity  | varchar   | not null   | product quantity |
| product price     | varchar   | not null   | product price    |

### kontragents

| column | data_type | constraint | description        |
|--------|-----------|------------|--------------------|
| id     | integer   | not null   | kontragent's id    |
| name   | varchar   | not null   | kontragent's name  |
| phone  | integer   | not null   | kontragent's phone |
| city   | varchar   | not null   | kontragent's city  |

### products

| column | data_type | constraint | description          |
|--------|-----------|------------|----------------------|
| id     | integer   | not null   | product id           |
| name   | varchar   | not null   | product's name  |
| od_vymir  | integer   | not null   | unit of measure for the quantity of goods |
| pereriz   | varchar   | not null   | wire cross-sectional area  |

### stock

| column | data_type | constraint | description          |
|--------|-----------|------------|----------------------|
| id     | integer   | not null   | stock id     |
| id_produkt   | integer   | not null   | product id   |
| id_manufacturer  | integer   | not null   | manufacturer id |
| product quantity   | varchar   | not null   | product quantity  |

### manufacturers

| column | data_type | constraint | description          |
|--------|-----------|------------|----------------------|
| id     | integer   | not null   | manufacturers id     |
| name   | varchar   | not null   | manufacturer's name  |
| phone  | integer   | not null   | manufacturer's phone |
| city   | varchar   | not null   | manufacturer's city  |