# goit-rdb-hw-02
## Relational databases Home Work 2

### Initial Table

| order_number | item_name_and_quantity | customer_address | order_date | customer   |
|--------------|------------------------|------------------|------------|------------|
| 101          | Laptop: 3, Mouse: 2    | Khreschatyk 1    | 2023-03-15 | Melnyk     |
| 102          | Printer: 1             | Baseyna 2        | 2023-03-16 | Shevchenko |
| 103          | Mouse: 4               | Compyuterna 3    | 2023-03-17 | Kovalenko  |

### 1NF

| order_number | item_name | quantity | customer_address | order_date | customer   |
|--------------|-----------|----------|------------------|------------|------------|
| 101          | Laptop    | 3        | Khreschatyk 1    | 2023-03-15 | Melnyk     |
| 101          | Mouse     | 2        | Khreschatyk 1    | 2023-03-15 | Melnyk     |
| 102          | Printer   | 1        | Baseyna 2        | 2023-03-16 | Shevchenko |
| 103          | Mouse     | 4        | Compyuterna 3    | 2023-03-17 | Kovalenko  |

### 2NF

#### Orders table

| order_number | customer_address | order_date | customer   |
|--------------|------------------|------------|------------|
| 101          | Khreschatyk 1    | 2023-03-15 | Melnyk     |
| 102          | Baseyna 2        | 2023-03-16 | Shevchenko |
| 103          | Compyuterna 3    | 2023-03-17 | Kovalenko  |

#### OrderItems table

| order_number | item_name | quantity |
|--------------|-----------|----------|
| 101          | Laptop    | 3        |
| 101          | Mouse     | 2        |
| 102          | Printer   | 1        |
| 103          | Mouse     | 4        |

### 3NF

#### Orders table

| order_number | order_date | customer   |
|--------------|------------|------------|
| 101          | 2023-03-15 | Melnyk     |
| 102          | 2023-03-16 | Shevchenko |
| 103          | 2023-03-17 | Kovalenko  |

#### OrderItems table 

| order_number | item_name | quantity |
|--------------|-----------|----------|
| 101          | Laptop    | 3        |
| 101          | Mouse     | 2        |
| 102          | Printer   | 1        |
| 103          | Mouse     | 4        |

#### Customers table

| customer   | customer_address |
|------------|------------------|
| Melnyk     | Khreschatyk 1    |
| Shevchenko | Baseyna 2        |
| Kovalenko  | Compyuterna 3    |
