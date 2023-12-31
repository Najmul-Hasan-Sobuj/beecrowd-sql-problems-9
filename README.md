### beecrowd SQL | 2602 - Customer Survey in Rio Grande do Sul

<details>

<summary>Click Here</summary>


**Author:** [Your Name or Institution]

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

Your company is conducting a survey to find out how many customers are registered in the states, specifically in 'Rio Grande do Sul'. You are required to display the names of all customers whose state is 'RS'.

#### Schema:

1. **Table: `customers`**

   | Column        | Type             |
   | ------------- | ---------------- |
   | id (PK)       | numeric          |
   | name          | varchar          |
   | street        | varchar          |
   | city          | varchar          |
   | state         | char             |
   | credit_limit  | number           |

#### Sample Data:

- **customers:**

  | id | name                      | street                   | city          | state | credit_limit |
  | -- | ------------------------- | ------------------------ | ------------- | ----- | ------------ |
  | 1  | Pedro Augusto da Rocha    | Rua Pedro Carlos Hoffman | Porto Alegre  | RS    | 700.00       |
  | 2  | Antonio Carlos Mamel      | Av. Pinheiros            | Belo Horizonte| MG    | 3500.50      |
  | 3  | Luiza Augusta Mhor        | Rua Salto Grande         | Niteroi       | RJ    | 4000.00      |
  | 4  | Jane Ester                | Av 7 de setembro         | Erechim       | RS    | 800.00       |
  | 5  | Marcos Antônio dos Santos | Av Farrapos              | Porto Alegre  | RS    | 4250.25      |

#### Task:

Write an SQL query to find the names of all customers whose state is 'RS'.

#### Output Sample:

| name                       |
| -------------------------- |
| Pedro Augusto da Rocha     |
| Jane Ester                 |
| Marcos Antônio dos Santos  |

---

#### SQL Query:

```sql
SELECT name
FROM customers
WHERE state = 'RS';
```

#### Explanation of the Query:

- `SELECT name`: This line specifies that we are interested in the `name` column from the `customers` table.

- `FROM customers`: The query begins by selecting data from the `customers` table.

- `WHERE state = 'RS'`: This condition filters the records to include only those customers who are from the state of 'RS'.

This query will list the names of all customers who are registered in the state of 'Rio Grande do Sul'.

</details> 


### beecrowd SQL | 2620 - Orders in First Half

<details>

<summary>Click Here</summary>


**Author:** Paulo R. Rodegheri, BR Brasil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The company's financial audit requires a report for the first half of 2016. The task is to display the customer's name and order number for customers who placed orders in the first half of 2016.

#### Schema:

1. **Table: `customers`**

   | Column        | Type                    |
   | ------------- | ----------------------- |
   | id (PK)       | numeric                 |
   | name          | character varying (255) |
   | street        | character varying (255) |
   | city          | character varying (255) |
   | state         | char (2)                |
   | credit\_limit | numeric                 |

2. **Table: `orders`**

   | Column             | Type           |
   | ------------------ | -------------- |
   | id (PK)            | numeric        |
   | orders\_date       | date (ISO/YMD) |
   | id\_customers (FK) | numeric        |

#### Sample Data:

- **customers:**

  | id | name                                    | street                                | city          | state | credit\_limit |
  | -- | --------------------------------------- | ------------------------------------- | ------------- | ----- | ------------- |
  | 1  | Nicolas Diogo Cardoso                   | Acesso Um                             | Porto Alegre  | RS    | 475           |
  | 2  | Cecília Olivia Rodrigues                | Rua Sizuka Usuy                       | Cianorte      | PR    | 3170          |
  | 3  | Augusto Fernando Carlos Eduardo Cardoso | Rua Baldomiro Koerich                 | Palhoça       | SC    | 1067          |
  | 4  | Nicolas Diogo Cardoso                   | Acesso Um                             | Porto Alegre  | RS    | 475           |
  | 5  | Sabrina Heloisa Gabriela Barros         | Rua Engenheiro Tito Marques Fernandes | Porto Alegre  | RS    | 4312          |
  | 6  | Joaquim Diego Lorenzo Araújo            | Rua Vitorino                          | Novo Hamburgo | RS    | 2314          |

- **orders:**

  | id | orders\_date | id\_customers |
  | -- | ------------ | ------------- |
  | 1  | 2016-05-13   | 3             |
  | 2  | 2016-01-12   | 2             |
  | 3  | 2016-04-18   | 5             |
  | 4  | 2016-09-07   | 4             |
  | 5  | 2016-02-13   | 6             |
  | 6  | 2016-08-05   | 3             |

#### Task:

Write an SQL query to find the names of customers and their order IDs for orders that were placed in the first half of 2016.

#### Output Sample:

| name                                    | id |
| --------------------------------------- | -- |
| Augusto Fernando Carlos Eduardo Cardoso | 1  |
| Cecília Olivia Rodrigues                | 2  |
| Sabrina Heloisa Gabriela Barros         | 3  |
| Joaquim Diego Lorenzo Araújo            | 5  |

---

#### SQL Query:

```sql
SELECT customers.name, orders.id
FROM customers
JOIN orders ON customers.id = orders.id_customers
WHERE orders.orders_date BETWEEN '2016-01-01' AND '2016-06-30';
```

#### Explanation of the Query:

- `SELECT customers.name, orders.id`: This line specifies that we are interested in the `name` column from the `customers` table and the `id` column from the `orders` table.

- `FROM customers`: The query begins by selecting data from the `customers` table.

- `JOIN orders ON customers.id = orders.id_customers`: Here, we perform an inner join with the `orders` table. The join condition is that the `id` field in the `customers` table should match the `id_customers` field in the `orders` table, ensuring each order is correctly associated with its customer.

- `WHERE orders.orders_date BETWEEN '2016-01-01' AND '2016-06-30'`: This condition filters the records to include only those orders that were placed between January 1, 2016, and June 30, 2016.

This table represents the names of the customers who placed orders in the first half of 2016, along with the IDs of those orders.

</details> 