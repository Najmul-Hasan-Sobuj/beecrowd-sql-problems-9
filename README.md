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
<!-- ```end -->

### beecrowd SQL | 2603 - Customer Address for 20th Anniversary Event

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The company is planning an event to celebrate its 20th anniversary in the market, with a grand celebration in Porto Alegre. All customers residing in Porto Alegre are invited. Your task is to obtain the names and addresses of customers living in 'Porto Alegre' to personally deliver the invitations.

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

Write an SQL query to find the names and streets of customers who live in 'Porto Alegre', to deliver the invitations personally.

#### Output Sample:

| name                      | street                   |
| ------------------------- | ------------------------ |
| Pedro Augusto da Rocha    | Rua Pedro Carlos Hoffman |
| Marcos Antônio dos Santos | Av Farrapos              |

---

#### SQL Query:

```sql
SELECT name, street
FROM customers
WHERE city = 'Porto Alegre';
```

#### Explanation of the Query:

- `SELECT name, street`: This line specifies that we are interested in the `name` and `street` columns from the `customers` table.

- `FROM customers`: The query begins by selecting data from the `customers` table.

- `WHERE city = 'Porto Alegre'`: This condition filters the records to include only those customers who live in Porto Alegre.

This query will provide the names and addresses of customers living in Porto Alegre for the purpose of personal invitation delivery to the company's 20th-anniversary celebration.

</details> 
<!-- ```end -->

### beecrowd SQL | 2604 - Under 10 or Greater Than 100

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The financial sector of the company requires a report listing the ID and the name of the products whose price is either less than 10 or greater than 100.

#### Schema:

1. **Table: `products`**

   | Column | Type    |
   | ------ | ------- |
   | id (PK)| numeric |
   | name   | varchar |
   | amount | numeric |
   | price  | numeric |

#### Sample Data:

- **products:**

  | id | name             | amount | price  |
  | -- | ---------------- | ------ | ------ |
  | 1  | Two-door wardrobe| 100    | 80     |
  | 2  | Dining table     | 1000   | 560    |
  | 3  | Towel holder     | 10000  | 5.50   |
  | 4  | Computer desk    | 350    | 100    |
  | 5  | Chair            | 3000   | 210.64 |
  | 6  | Single bed       | 750    | 99     |

#### Task:

Write an SQL query to find the ID and name of products whose price is less than 10 or greater than 100.

#### Output Sample:

| id | name         |
| -- | ------------ |
| 2  | Dining table |
| 3  | Towel holder |
| 5  | Chair        |

---

#### SQL Query:

```sql
SELECT id, name
FROM products
WHERE price < 10 OR price > 100;
```

#### Explanation of the Query:

- `SELECT id, name`: This line specifies that we are interested in the `id` and `name` columns from the `products` table.

- `FROM products`: The query begins by selecting data from the `products` table.

- `WHERE price < 10 OR price > 100`: This condition filters the records to include only those products whose price is either less than 10 or greater than 100.

This query will provide the IDs and names of products that meet the specified price criteria for the financial sector's report.

</details> 
<!-- ```end -->

### beecrowd SQL | 2605 - Executive Representatives

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The financial sector needs a report on the providers of the products we sell, particularly those in the 'executive' category (category ID 6). The task is to return the names of the products and providers whose category ID is 6.

#### Schema:

1. **Table: `products`**

   | Column             | Type    |
   | ------------------ | ------- |
   | id (Primary Key)   | numeric |
   | name               | varchar |
   | amount             | numeric |
   | price              | numeric |
   | id_providers       | numeric |
   | id_categories      | numeric |

2. **Table: `providers`**

   | Column             | Type    |
   | ------------------ | ------- |
   | id (Primary Key)   | numeric |
   | name               | varchar |
   | street             | varchar |
   | city               | varchar |
   | state              | char    |

3. **Table: `categories`**

   | Column             | Type    |
   | ------------------ | ------- |
   | id (Primary Key)   | numeric |
   | name               | varchar |

#### Sample Data:

- **products:**

  | id | name             | amount | price  | id_providers | id_categories |
  | -- | ---------------- | ------ | ------ | ------------ | ------------- |
  | 1  | Two-door wardrobe| 100    | 800    | 6            | 8             |
  | 2  | Dining table     | 1000   | 560    | 1            | 9             |
  | 3  | Towel holder     | 10000  | 25.50  | 5            | 1             |
  | 4  | Computer desk    | 350    | 320.50 | 4            | 6             |
  | 5  | Chair            | 3000   | 210.64 | 3            | 6             |
  | 6  | Single bed       | 750    | 460    | 1            | 2             |

- **providers:**

  | id | name             | street          | city           | state |
  | -- | ---------------- | --------------- | -------------- | ----- |
  | 1  | Henrique         | Av Brasil       | Rio de Janeiro | RJ    |
  | 2  | Marcelo Augusto  | Rua Imigrantes  | Belo Horizonte | MG    |
  | 3  | Caroline Silva   | Av São Paulo    | Salvador       | BA    |
  | 4  | Guilerme Staff   | Rua Central     | Porto Alegre   | RS    |
  | 5  | Isabela Moraes   | Av Juiz Grande  | Curitiba       | PR    |
  | 6  | Francisco Accerr | Av Paulista     | São Paulo      | SP    |

- **categories:**

  | id | name         |
  | -- | ------------ |
  | 1  | old stock    |
  | 2  | new stock    |
  | 3  | modern       |
  | 4  | commercial   |
  | 5  | recyclable   |
  | 6  | executive    |
  | 7  | superior     |
  | 8  | wood         |
  | 9  | super luxury |
  | 10 | vintage      |

#### Task:

Write an SQL query to return the names of the products and their providers for products whose category ID is 6.

#### Output Sample:

| Product Name  | Provider Name   |
| ------------- | --------------- |
| Computer desk | Guilerme Staff  |
| Chair         | Caroline Silva  |

---

#### SQL Query:

```sql
SELECT products.name AS Product Name, providers.name AS Provider Name
FROM products
JOIN providers ON products.id_providers = providers.id
WHERE products.id_categories = 6;
```

#### Explanation of the Query:

- `SELECT products.name AS Product Name, providers.name AS Provider Name`: This line specifies that we are interested in the `name` columns from both the `products` and `providers` tables, aliasing them as Product Name and Provider Name, respectively.

- `FROM products`: The query begins by selecting data from the `products` table.

- `JOIN providers ON products.id_providers = providers.id`: Here, an inner join is performed with the `providers` table. The join condition is that the `id_providers` field in the `products` table should match the `id` field in the

 `providers` table.

- `WHERE products.id_categories = 6`: This condition filters the records to include only those products whose category ID is 6.

This query will provide the names of the products and their providers for products in the 'executive' category.

</details> 
<!-- ```end -->

### beecrowd SQL | 2606 - Categories Starting with 'super'

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

There was a misunderstanding during data migration to the database. Your task is to select the ID and the name of the products, whose category name starts with 'super'.

#### Schema:

1. **Table: `products`**

   | Column             | Type    |
   | ------------------ | ------- |
   | id (Primary Key)   | numeric |
   | name               | varchar |
   | amount             | numeric |
   | price              | numeric |
   | id_categories (FK) | numeric |

2. **Table: `categories`**

   | Column             | Type    |
   | ------------------ | ------- |
   | id (Primary Key)   | numeric |
   | name               | varchar |

#### Sample Data:

- **products:**

  | id | name               | amount | price | id_categories |
  | -- | ------------------ | ------ | ----- | ------------- |
  | 1  | Lampshade          | 100    | 800   | 4             |
  | 2  | Table for painting | 1000   | 560   | 9             |
  | 3  | Notebook desk      | 10000  | 25.50 | 9             |
  | 4  | Computer desk      | 350    | 320.50| 6             |
  | 5  | Chair              | 3000   | 210.64| 9             |
  | 6  | Home alarm         | 750    | 460   | 4             |

- **categories:**

  | id | name         |
  | -- | ------------ |
  | 1  | old stock    |
  | 2  | new stock    |
  | 3  | modern       |
  | 4  | commercial   |
  | 5  | recyclable   |
  | 6  | executive    |
  | 7  | superior     |
  | 8  | wood         |
  | 9  | super luxury |
  | 10 | vintage      |

#### Task:

Write an SQL query to select the ID and name of products whose category name starts with 'super'.

#### Output Sample:

| id | name               |
| -- | ------------------ |
| 2  | Table for painting |
| 3  | Notebook desk      |
| 5  | Chair              |

---

#### SQL Query:

```sql
SELECT products.id, products.name
FROM products
JOIN categories ON products.id_categories = categories.id
WHERE categories.name LIKE 'super%';
```

#### Explanation of the Query:

- `SELECT products.id, products.name`: This line specifies that we are interested in the `id` and `name` columns from the `products` table.

- `FROM products`: The query begins by selecting data from the `products` table.

- `JOIN categories ON products.id_categories = categories.id`: Here, an inner join is performed with the `categories` table. The join condition is that the `id_categories` field in the `products` table should match the `id` field in the `categories` table.

- `WHERE categories.name LIKE 'super%'`: This condition filters the records to include only those products whose category name starts with 'super'.

This query will provide the IDs and names of products in categories that begin with 'super'.

</details> 
<!-- ```end -->

### beecrowd SQL | 2607 - Providers' City in Alphabetical Order

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

Every month, the company requires a report listing the cities where providers are registered. The task is to create a query that returns all the cities of the providers, sorted in alphabetical order, ensuring that each city is listed only once.

#### Schema:

1. **Table: `providers`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |
   | street | varchar |
   | city   | varchar |
   | state  | char    |

#### Sample Data:

- **providers:**

  | id | name            | street         | city           | state |
  | -- | --------------- | -------------- | -------------- | ----- |
  | 1  | Henrique        | Av Brasil      | Rio de Janeiro | RJ    |
  | 2  | Marcelo Augusto | Rua Imigrantes | Belo Horizonte | MG    |
  | 3  | Caroline Silva  | Av São Paulo   | Salvador       | BA    |
  | 4  | Guilerme Staff  | Rua Central    | Porto Alegre   | RS    |
  | 5  | Isabela Moraes  | Av Juiz Grande | Curitiba       | PR    |
  | 6  | Francisco Accerr| Av Paulista    | São Paulo      | SP    |

#### Task:

Write an SQL query to return a list of cities where providers are registered, sorted in alphabetical order without duplicates.

#### Output Sample:

| city           |
| -------------- |
| Belo Horizonte |
| Curitiba       |
| Porto Alegre   |
| Rio de Janeiro |
| Salvador       |
| São Paulo      |

---

#### SQL Query:

```sql
SELECT DISTINCT city
FROM providers
ORDER BY city ASC;
```

#### Explanation of the Query:

- `SELECT DISTINCT city`: This line specifies that we are interested in the unique instances of the `city` column from the `providers` table. The `DISTINCT` keyword ensures that each city is listed only once.

- `FROM providers`: The query selects data from the `providers` table.

- `ORDER BY city ASC`: This part of the query sorts the results in ascending alphabetical order based on the city names.

This query will provide a list of unique cities where providers are registered, sorted alphabetically.

</details> 
<!-- ```end -->

### beecrowd SQL | 2608 - Higher and Lower Price

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The financial sector of our company is interested in knowing the highest and lowest prices of the products we sell. The task is to display only the highest and lowest price from the products table.

#### Schema:

1. **Table: `products`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |
   | amount | numeric |
   | price  | numeric |

#### Sample Data:

- **products:**

  | id | name               | amount | price  |
  | -- | ------------------ | ------ | ------ |
  | 1  | Two-doors wardrobe | 100    | 800    |
  | 2  | Dining table       | 1000   | 560    |
  | 3  | Towel holder       | 10000  | 25.50  |
  | 4  | Computer desk      | 350    | 320.50 |
  | 5  | Chair              | 3000   | 210.64 |
  | 6  | Single bed         | 750    | 460    |

#### Task:

Write an SQL query to find the highest and lowest price of the products.

#### Output Sample:

| Highest Price | Lowest Price |
| ------------- | ------------ |
| 800           | 25.50        |

---

#### SQL Query:

```sql
SELECT MAX(price) AS 'Highest Price', MIN(price) AS 'Lowest Price'
FROM products;
```

#### Explanation of the Query:

- `SELECT MAX(price) AS 'Highest Price', MIN(price) AS 'Lowest Price'`: This line specifies that we are interested in the maximum (highest) and minimum (lowest) values of the `price` column from the `products` table. The results are aliased as 'Highest Price' and 'Lowest Price' for clarity.

- `FROM products`: The query selects data from the `products` table.

This query will provide the highest and lowest prices of the products sold by the company.

</details> 
<!-- ```end -->

### beecrowd SQL | 2609 - Products by Categories

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The sales industry is conducting an analysis of the number of products in stock. Your task is to display the name and the total amount of products for each category.

#### Schema:

1. **Table: `products`**

   | Column             | Type    |
   | ------------------ | ------- |
   | id (Primary Key)   | numeric |
   | name               | varchar |
   | amount             | numeric |
   | price              | numeric |
   | id_categories (FK) | numeric |

2. **Table: `categories`**

   | Column             | Type    |
   | ------------------ | ------- |
   | id (Primary Key)   | numeric |
   | name               | varchar |

#### Sample Data:

- **products:**

  | id | name              | amount | price | id_categories |
  | -- | ----------------- | ------ | ----- | ------------- |
  | 1  | Two-doors wardrobe| 100    | 800   | 1             |
  | 2  | Dining table      | 1000   | 560   | 3             |
  | 3  | Towel holder      | 10000  | 25.50 | 4             |
  | 4  | Computer desk     | 350    | 320.50| 2             |
  | 5  | Chair             | 3000   | 210.64| 4             |
  | 6  | Single bed        | 750    | 460   | 1             |

- **categories:**

  | id | name         |
  | -- | ------------ |
  | 1  | wood         |
  | 2  | luxury       |
  | 3  | vintage      |
  | 4  | modern       |
  | 5  | super luxury |

#### Task:

Write an SQL query to display the name and the total amount of products for each category.

#### Output Sample:

| Category Name | Total Amount |
| ------------- | ------------ |
| luxury        | 350          |
| modern        | 13000        |
| wood          | 850          |
| vintage       | 1000         |

---

#### SQL Query:

```sql
SELECT categories.name AS 'Category Name', SUM(products.amount) AS 'Total Amount'
FROM products
JOIN categories ON products.id_categories = categories.id
GROUP BY categories.name;
```

#### Explanation of the Query:

- `SELECT categories.name AS 'Category Name', SUM(products.amount) AS 'Total Amount'`: This line specifies that we are interested in the `name` column from the `categories` table and the sum of the `amount` column from the `products` table. The results are aliased as 'Category Name' and 'Total Amount' for clarity.

- `FROM products`: The query begins by selecting data from the `products` table.

- `JOIN categories ON products.id_categories = categories.id`: This part performs an inner join with the `categories` table. The join condition is that the `id_categories` field in the `products` table should match the `id` field in the `categories` table.

- `GROUP BY categories.name`: This clause groups the results by the category names, allowing the `SUM` function to calculate the total amount of products per category.

This query will provide the names of the categories along with the total amount of products in each category.

</details> 
<!-- ```end -->

### beecrowd SQL | 2610 - Average Value of Products

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

In the company where you work, a survey is being conducted on the values of the marketed products. Your task is to calculate and display the average value of the price of the products. Note: Show the value with two decimal places.

#### Schema:

1. **Table: `products`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |
   | amount | numeric |
   | price  | numeric |

#### Sample Data:

- **products:**

  | id | name               | amount | price  |
  | -- | ------------------ | ------ | ------ |
  | 1  | Two-doors wardrobe | 100    | 800    |
  | 2  | Dining table       | 1000   | 560    |
  | 3  | Towel holder       | 10000  | 25.50  |
  | 4  | Computer desk      | 350    | 320.50 |
  | 5  | Chair              | 3000   | 210.64 |
  | 6  | Single bed         | 750    | 460    |

#### Task:

Write an SQL query to find the average value of the price of the products.

#### Output Sample:

| Average Price |
| ------------- |
| 396.10        |

---

#### SQL Query:

```sql
-- Your SQL query will go here
```

#### Explanation of the Query:

- Provide a brief explanation of your SQL query here.

This query will provide the average price of the products sold by the company.

</details> 
<!-- ```end -->

### beecrowd SQL | 2611 - Action Movies

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

A video store contractor has hired your services for cataloging movies. Your task is to select the code and the name of the movies whose genre description is 'Action'.

#### Schema:

1. **Table: `movies`**

   | Column      | Type    |
   | ----------- | ------- |
   | id (Primary Key) | numeric |
   | name        | varchar |
   | id_genres (Foreign Key)  | numeric |

2. **Table: `genres`**

   | Column      | Type    |
   | ----------- | ------- |
   | id (Primary Key) | numeric |
   | description | varchar |

#### Sample Data:

- **movies:**

  | id | name                         | id_genres |
  | -- | ---------------------------- | --------- |
  | 1  | Batman                       | 3         |
  | 2  | The Battle of the Dark River | 3         |
  | 3  | White Duck                   | 1         |
  | 4  | Breaking Barriers            | 4         |
  | 5  | The Two Hours                | 2         |

- **genres:**

  | id | description |
  | -- | ----------- |
  | 1  | Animation   |
  | 2  | Horror      |
  | 3  | Action      |
  | 4  | Drama       |
  | 5  | Comedy      |

#### Task:

Write an SQL query to find the code and name of movies categorized as 'Action'.

#### Output Sample:

| id | name                      |
| -- | ------------------------- |
| 1  | Batman                    |
| 2  | The Battle of the Dark River |

---

#### SQL Query:

```sql
SELECT movies.id, movies.name
FROM movies
JOIN genres ON movies.id_genres = genres.id
WHERE genres.description = 'Action';
```

#### Explanation of the Query:

- `SELECT movies.id, movies.name`: Selects the ID and name of the movies from the `movies` table.

- `FROM movies`: Indicates that the data is being retrieved from the `movies` table.

- `JOIN genres ON movies.id_genres = genres.id`: Joins the `movies` table with the `genres` table based on the foreign key relationship, linking each movie to its genre.

- `WHERE genres.description = 'Action'`: Filters the results to include only movies whose genre is described as 'Action'.

This query will retrieve the code and names of movies that are categorized as 'Action' in the store's catalog.

</details> 
<!-- ```end -->

### beecrowd SQL | 2613 - Cheap Movies

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The studio previously held an event where several movies were on sale. The task is to identify these movies by selecting the ID and name of movies whose price is less than 2.00.

#### Schema:

1. **Table: `movies`**

   | Column      | Type    |
   | ----------- | ------- |
   | id (Primary Key) | numeric |
   | name        | varchar |
   | id_prices (Foreign Key) | numeric |

2. **Table: `prices`**

   | Column      | Type    |
   | ----------- | ------- |
   | id (Primary Key) | numeric |
   | categorie   | varchar |
   | value       | numeric |

#### Sample Data:

- **movies:**

  | id | name                         | id_prices |
  | -- | ---------------------------- | --------- |
  | 1  | Batman                       | 3         |
  | 2  | The Battle of the Dark River | 3         |
  | 3  | White Duck                   | 5         |
  | 4  | Breaking Barriers            | 4         |
  | 5  | The Two Hours                | 2         |

- **prices:**

  | id | categorie    | value |
  | -- | ------------ | ----- |
  | 1  | Releases     | 3.50  |
  | 2  | Bronze Seal  | 2.00  |
  | 3  | Silver Seal  | 2.50  |
  | 4  | Gold Seal    | 3.00  |
  | 5  | Promotion    | 1.50  |

#### Task:

Write an SQL query to find the ID and name of movies with a price less than 2.00.

#### Output Sample:

| id | name       |
| -- | ---------- |
| 3  | White Duck |

---

#### SQL Query:

```sql
SELECT movies.id, movies.name
FROM movies
JOIN prices ON movies.id_prices = prices.id
WHERE prices.value < 2.00;
```

#### Explanation of the Query:

- `SELECT movies.id, movies.name`: This selects the ID and name of the movies from the `movies` table.

- `FROM movies`: Indicates that the data is being retrieved from the `movies` table.

- `JOIN prices ON movies.id_prices = prices.id`: Joins the `movies` table with the `prices` table based on the foreign key relationship, linking each movie to its associated price category.

- `WHERE prices.value < 2.00`: Filters the results to include only those movies with a price value of less than 2.00.

This query will retrieve the ID and names of movies priced under 2.00 during the studio's sale event.

</details> 
<!-- ```end -->

### beecrowd SQL | 2614 - September Rentals

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The video store is preparing its semi-annual report and requires assistance. The task is to select the names of the clients and the dates of rental for all rentals made in September 2016.

#### Schema:

1. **Table: `customers`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |
   | street | varchar |
   | city   | varchar |

2. **Table: `rentals`**

   | Column          | Type    |
   | --------------- | ------- |
   | id (Primary Key) | numeric |
   | rentals_date    | date (ISO/YMD) |
   | id_customers (Foreign Key) | numeric |

#### Sample Data:

- **customers:**

  | id | name                     | street                            | city          |
  | -- | ------------------------ | --------------------------------- | ------------- |
  | 1  | Giovanna Goncalves Oliveira | Rua Mato Grosso                    | Canoas        |
  | 2  | Kauã Azevedo Ribeiro      | Travessa Ibiá                      | Uberlândia    |
  | 3  | Rebeca Barbosa Santos     | Rua Observatório Meteorológico     | Salvador      |
  | 4  | Sarah Carvalho Correia    | Rua Antônio Carlos da Silva        | Apucarana     |
  | 5  | João Almeida Lima         | Rua Rio Taiuva                     | Ponta Grossa  |
  | 6  | Diogo Melo Dias           | Rua Duzentos e Cinqüenta           | Várzea Grande |

- **rentals:**

  | id | rentals_date | id_customers |
  | -- | ------------ | ------------ |
  | 1  | 2016-09-10   | 3            |
  | 2  | 2016-02-09   | 1            |
  | 3  | 2016-02-08   | 4            |
  | 4  | 2016-02-09   | 2            |
  | 5  | 2016-02-03   | 6            |
  | 6  | 2016-04-04   | 4            |

#### Task:

Write an SQL query to find the names of clients and the rental dates for all rentals made in September 2016.

#### Output Sample:

| name                  | rentals_date |
| --------------------- | ------------ |
| Rebeca Barbosa Santos | 2016-09-10   |

---

#### SQL Query:

```sql
SELECT customers.name, rentals.rentals_date
FROM rentals
JOIN customers ON rentals.id_customers = customers.id
WHERE EXTRACT(MONTH FROM rentals.rentals_date) = 9 AND EXTRACT(YEAR FROM rentals.rentals_date) = 2016;
```

#### Explanation of the Query:

- `SELECT customers.name, rentals.rentals_date`: This selects the name from the `customers` table and the rentals_date from the `rentals` table.

- `FROM rentals`: Indicates that the data is being retrieved from the `rentals` table.

- `JOIN customers ON rentals.id_customers = customers.id`: Joins the `rentals` table with the `customers` table based on the foreign key relationship, linking each rental to its respective customer.

- `WHERE EXTRACT(MONTH FROM rentals.rentals_date) = 9 AND EXTRACT(YEAR FROM rentals.rentals_date) = 2016`: Filters the results to include only rentals that occurred in September 2016.

This query will retrieve the names of customers and the dates of their rentals for September 2016.

</details> 
<!-- ```end -->

### beecrowd SQL | 2615 - Expanding the Business

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The video store company aims to create several franchises across Brazil. To assist in this expansion, we need to know the cities where our customers reside. The task is to select the names of all the cities where the rental company has clients, ensuring that each city name is listed only once.

#### Schema:

1. **Table: `customers`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |
   | street | varchar |
   | city   | varchar |

#### Sample Data:

- **customers:**

  | id | name                     | street                            | city           |
  | -- | ------------------------ | --------------------------------- | -------------- |
  | 1  | Giovanna Goncalves Oliveira | Rua Mato Grosso                    | Canoas         |
  | 2  | Kauã Azevedo Ribeiro      | Travessa Ibiá                      | Uberlândia     |
  | 3  | Rebeca Barbosa Santos     | Rua Observatório Meteorológico     | Salvador       |
  | 4  | Sarah Carvalho Correia    | Rua Antônio Carlos da Silva        | Uberlândia     |
  | 5  | João Almeida Lima         | Rua Rio Taiuva                     | Ponta Grossa   |
  | 6  | Diogo Melo Dias           | Rua Duzentos e Cinqüenta           | Várzea Grande  |

#### Task:

Write an SQL query to find the names of all cities where the company's clients reside, without repeating any city name.

#### Output Sample:

| city           |
| -------------- |
| Uberlândia     |
| Canoas         |
| Ponta Grossa   |
| Várzea Grande  |
| Salvador       |

---

#### SQL Query:

```sql
SELECT DISTINCT city
FROM customers;
```

#### Explanation of the Query:

- `SELECT DISTINCT city`: This command selects the `city` column from the `customers` table. The `DISTINCT` keyword ensures that each city name appears only once in the result set, even if it occurs multiple times in the table.

- `FROM customers`: Indicates that the data is being retrieved from the `customers` table.

This query will provide a list of unique city names where the company's clients reside, aiding in the strategic planning for business expansion.

</details> 
<!-- ```end -->

### beecrowd SQL | 2616 - No Rental

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The video store company is planning a promotion for customers who have not yet made any rentals. The task is to identify these customers by delivering the ID and the name of customers who have not engaged in any rentals. The output should be sorted by ID.

#### Schema:

1. **Table: `customers`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |
   | street | varchar |
   | city   | varchar |

2. **Table: `locations`**

   | Column          | Type    |
   | --------------- | ------- |
   | id (Primary Key) | numeric |
   | locations_date   | date (ISO/YMD) |
   | id_customers (Foreign Key) | numeric |

#### Sample Data:

- **customers:**

  | id | name                     | street                            | city           |
  | -- | ------------------------ | --------------------------------- | -------------- |
  | 1  | Giovanna Goncalves Oliveira | Rua Mato Grosso                    | Canoas         |
  | 2  | Kauã Azevedo Ribeiro      | Travessa Ibiá                      | Uberlândia     |
  | 3  | Rebeca Barbosa Santos     | Rua Observatório Meteorológico     | Salvador       |
  | 4  | Sarah Carvalho Correia    | Rua Antônio Carlos da Silva        | Apucarana      |
  | 5  | João Almeida Lima         | Rua Rio Taiuva                     | Ponta Grossa   |
  | 6  | Diogo Melo Dias           | Rua Duzentos e Cinqüenta           | Várzea Grande  |

- **locations:**

  | id | locations_date | id_customers |
  | -- | -------------- | ------------ |
  | 1  | 2016-10-09     | 3            |
  | 2  | 2016-09-02     | 1            |
  | 3  | 2016-08-02     | 4            |
  | 4  | 2016-09-02     | 2            |
  | 5  | 2016-03-02     | 6            |
  | 6  | 2016-04-04     | 4            |

#### Task:

Write an SQL query to find the ID and name of customers who have not made any rentals. The results should be ordered by ID.

#### Output Sample:

| id | name             |
| -- | ---------------- |
| 5  | João Almeida Lima |

---

#### SQL Query:

```sql
SELECT customers.id, customers.name
FROM customers
LEFT JOIN locations ON customers.id = locations.id_customers
WHERE locations.id_customers IS NULL
ORDER BY customers.id;
```

#### Explanation of the Query:

- `SELECT customers.id, customers.name`: This selects the ID and name of the customers from the `customers` table.

- `FROM customers`: Indicates that the data is being retrieved from the `customers` table.

- `LEFT JOIN locations ON customers.id = locations.id_customers`: Performs a left join of the `customers` table with the `locations` table. This join includes all customers, whether or not they have made any rentals.

- `WHERE locations.id_customers IS NULL`: Filters the results to include only those customers who have not made any rentals. This is determined by checking for null values in the `id_customers` column of the `locations` table, which indicates no rental activity for that customer.

- `ORDER BY customers.id`: Orders the resulting data by the customer ID.

This query identifies customers who have not engaged in any rentals, aiding in targeting them for the company's promotional activities.

</details> 
<!-- ```end -->

### beecrowd SQL | 2617 - Provider Ajax SA

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The financial sector has encountered problems in the delivery from one of our providers, Ajax SA. The delivery of the products does not match the invoice. Your task is to display the name of the products and the name of the provider for the products supplied by 'Ajax SA'.

#### Schema:

1. **Table: `providers`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | street | character varying (255) |
   | city   | character varying (255) |
   | state  | char (2)               |

2. **Table: `products`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | amount | numeric               |
   | price  | numeric               |
   | id_providers (Foreign Key) | numeric  |

#### Sample Data:

- **providers:**

  | id | name       | street                   | city          | state |
  | -- | ---------- | ------------------------ | ------------- | ----- |
  | 1  | Ajax SA    | Presidente Castelo Branco | Porto Alegre | RS    |
  | 2  | Sansul SA  | Av Brasil                | Rio de Janeiro | RJ    |
  | 3  | South Chairs | Av Moinho              | Santa Maria   | RS    |
  | 4  | Elon Electro | Apolo                  | São Paulo     | SP    |
  | 5  | Mike Electro | Pedro da Cunha         | Curitiba      | PR    |

- **products:**

  | id | name             | amount | price   | id_providers |
  | -- | ---------------- | ------ | ------- | ------------ |
  | 1  | Blue Chair       | 30     | 300.00  | 5            |
  | 2  | Red Chair        | 50     | 2150.00 | 1            |
  | 3  | Disney Wardrobe  | 400    | 829.50  | 4            |
  | 4  | Blue Toaster     | 20     | 9.90    | 3            |
  | 5  | Solar Panel      | 30     | 3000.25 | 4            |

#### Task:

Write an SQL query to display the name of the products and the name of the provider for products supplied by 'Ajax SA'.

#### SQL Query:

```sql
SELECT products.name AS "Product Name", providers.name AS "Provider Name"
FROM products
JOIN providers ON products.id_providers = providers.id
WHERE providers.name = 'Ajax SA';
```

#### Explanation of the Query:

- `SELECT products.name AS "Product Name", providers.name AS "Provider Name"`: This line selects the `name` column from the `products` table and the `name` column from the `providers` table. The results are aliased as "Product Name" and "Provider Name" for clarity.

- `FROM products`: This specifies that the data is being selected from the `products` table.

- `JOIN providers ON products.id_providers = providers.id`: This line joins the `products` table with the `providers` table. The join condition is that the `id_providers` column in the `products` table matches the `id` column in the `providers` table.

- `WHERE providers.name = 'Ajax SA'`: This line filters the results to only include rows where the `name` column in the `providers` table is 'Ajax SA'. 

This query will display the names of the products and the corresponding provider name for those products supplied by 'Ajax SA'.

#### Output Sample:

| Product Name | Provider Name |
| ------------ | ------------- |
| Red Chair    | Ajax SA       |

---

</details> 
<!-- ```end -->

### beecrowd SQL | 2618 - Imported Products

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

Our company's import sector needs a report on the import of products from our Sansul providers. The task is to display the name of the products, the name of the supplier, and the name of the category for the products supplied by the supplier 'Sansul SA' and whose category name is 'Imported'.

#### Schema:

1. **Table: `products`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | amount | numeric               |
   | price  | numeric               |
   | id_providers (Foreign Key) | numeric  |
   | id_categories (Foreign Key) | numeric |

2. **Table: `providers`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | street | character varying (255) |
   | city   | character varying (255) |
   | state  | char (2)               |

3. **Table: `categories`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |

#### Sample Data:

- **products:**

  | id | name            | amount | price   | id_providers | id_categories |
  | -- | --------------- | ------ | ------- | ------------ | ------------- |
  | 1  | Blue Chair      | 30     | 300.00  | 5            | 5             |
  | 2  | Red Chair       | 50     | 2150.00 | 2            | 1             |
  | 3  | Disney Wardrobe | 400    | 829.50  | 4            | 1             |
  | 4  | Blue Toaster    | 20     | 9.90    | 3            | 1             |
  | 5  | TV              | 30     | 3000.25 | 2            | 2             |

- **providers:**

  | id | name       | street                   | city          | state |
  | -- | ---------- | ------------------------ | ------------- | ----- |
  | 1  | Ajax SA    | Rua Presidente Castelo Branco | Porto Alegre | RS    |
  | 2  | Sansul SA  | Av Brasil                | Rio de Janeiro | RJ    |
  | 3  | South Chairs | Rua do Moinho          | Santa Maria   | RS    |
  | 4  | Elon Electro | Rua Apolo              | São Paulo     | SP    |
  | 5  | Mike Electro | Rua Pedro da Cunha     | Curitiba      | PR    |

- **categories:**

  | id | name        |
  | -- | ----------- |
  | 1  | Super Luxury |
  | 2  | Imported    |
  | 3  | Tech        |
  | 4  | Vintage     |
  | 5  | Supreme     |

#### Task:

Write an SQL query to display the name of the products, the name of the supplier, and the name of the category for products supplied by 'Sansul SA' and whose category name is 'Imported'.

#### SQL Query:

```sql
SELECT products.name AS "Product Name", providers.name AS "Provider Name", categories.name AS "Category Name"
FROM products
JOIN providers ON products.id_providers = providers.id
JOIN categories ON products.id_categories = categories.id
WHERE providers.name = 'Sansul SA' AND categories.name = 'Imported';
```

#### Explanation of the Query:

- `SELECT products.name AS "Product Name", providers.name AS "Provider Name", categories.name AS "Category Name"`: This line selects the `name` column from each of the `products`, `providers`, and `categories` tables. The results are aliased for clarity.

- `FROM products`: Specifies the primary table from which to select data.

- `JOIN providers ON products.id_providers = providers.id`: Joins the `products` table with the `providers` table where the provider IDs match.

- `JOIN categories ON products.id_categories = categories.id`: Joins the `products` table with the `categories` table where the category IDs match.

- `WHERE providers.name = 'Sansul SA' AND categories.name = 'Imported'`: Filters the results to include only those products supplied by 'Sansul

 SA' and belonging to the 'Imported' category.

This query will display the required information about imported products supplied by 'Sansul SA'.

#### Output Sample:

| Product Name | Provider Name | Category Name |
| ------------ | ------------- | ------------- |
| TV           | Sansul SA     | Imported      |

---

</details> 
<!-- ```end -->

### beecrowd SQL | 2619 - Super Luxury

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

Our company is looking to make a new contract for the supply of new super luxury products. For this, we need some data about our current products. Your task is to display the name of the products, the name of the providers, and the price for the products whose price is greater than 1000 and whose category is 'Super Luxury'.

#### Schema:

1. **Table: `products`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | amount | numeric               |
   | price  | numeric               |
   | id_providers (Foreign Key) | numeric  |
   | id_categories (Foreign Key) | numeric |

2. **Table: `providers`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | street | character varying (255) |
   | city   | character varying (255) |
   | state  | char (2)               |

3. **Table: `categories`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |

#### Sample Data:

- **products:**

  | id | name            | amount | price   | id_providers | id_categories |
  | -- | --------------- | ------ | ------- | ------------ | ------------- |
  | 1  | Blue Chair      | 30     | 300.00  | 5            | 5             |
  | 2  | Red Chair       | 50     | 2150.00 | 2            | 1             |
  | 3  | Disney Wardrobe | 400    | 829.50  | 4            | 1             |
  | 4  | Blue Toaster    | 20     | 9.90    | 3            | 1             |
  | 5  | TV              | 30     | 3000.25 | 2            | 2             |

- **providers:**

  | id | name       | street                   | city          | state |
  | -- | ---------- | ------------------------ | ------------- | ----- |
  | 1  | Ajax SA    | Rua Presidente Castelo Branco | Porto Alegre | RS    |
  | 2  | Sansul SA  | Av Brasil                | Rio de Janeiro | RJ    |
  | 3  | South Chairs | Rua do Moinho          | Santa Maria   | RS    |
  | 4  | Elon Electro | Rua Apolo              | São Paulo     | SP    |
  | 5  | Mike Electro | Rua Pedro da Cunha     | Curitiba      | PR    |

- **categories:**

  | id | name        |
  | -- | ----------- |
  | 1  | Super Luxury |
  | 2  | Imported    |
  | 3  | Tech        |
  | 4  | Vintage     |
  | 5  | Supreme     |

#### Task:

Write an SQL query to display the name of the products, the name of the providers, and the price for products whose price is greater than 1000 and whose category is 'Super Luxury'.

#### SQL Query:

```sql
SELECT products.name AS "Product Name", providers.name AS "Provider Name", products.price AS "Price"
FROM products
JOIN providers ON products.id_providers = providers.id
JOIN categories ON products.id_categories = categories.id
WHERE products.price > 1000 AND categories.name = 'Super Luxury';
```

#### Explanation of the Query:

- `SELECT products.name AS "Product Name", providers.name AS "Provider Name", products.price AS "Price"`: This line selects the `name` and `price` columns from the `products` table and the `name` column from the `providers` table. The results are aliased for clarity.

- `FROM products`: Specifies the primary table from which to select data.

- `JOIN providers ON products.id_providers = providers.id`: Joins the `products` table with the `providers` table where the provider IDs match.

- `JOIN categories ON products.id_categories = categories.id`: Joins the `products` table with the `categories` table where the category IDs match.

- `WHERE products.price > 1000 AND categories.name = 'Super Luxury'`: Filters the results to include only those products whose

 price is greater than 1000 and which belong to the 'Super Luxury' category.

This query will display the required information for products in the 'Super Luxury' category with a price greater than 1000.

#### Output Sample:

| Product Name | Provider Name | Price    |
| ------------ | ------------- | -------- |
| Red Chair    | Sansul SA     | 2150.00  |

---

</details> 
<!-- ```end -->

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
<!-- ```end -->

### beecrowd SQL | 2621 - Amounts Between 10 and 20

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The stock keeper needs help with a report. The task is to display the name of products whose amount is between 10 and 20 and whose supplier's name starts with the letter 'P'.

#### Schema:

1. **Table: `providers`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | street | character varying (255) |
   | city   | character varying (255) |
   | state  | char (2)               |

2. **Table: `products`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | amount | numeric               |
   | price  | numeric               |
   | id_providers (Foreign Key) | numeric  |

#### Sample Data:

- **providers:**

  | id | name                | street                   | city          | state |
  | -- | ------------------- | ------------------------ | ------------- | ----- |
  | 1  | Ajax SA             | Rua Presidente Castelo Branco | Porto Alegre | RS    |
  | 2  | Sansul SA           | Av Brasil                | Rio de Janeiro | RJ    |
  | 3  | Pr Sheppard Chairs  | Rua do Moinho            | Santa Maria   | RS    |
  | 4  | Elon Electro        | Rua Apolo                | São Paulo     | SP    |
  | 5  | Mike Electro        | Rua Pedro da Cunha       | Curitiba      | PR    |

- **products:**

  | id | name             | amount | price   | id_providers |
  | -- | ---------------- | ------ | ------- | ------------ |
  | 1  | Blue Chair       | 30     | 300.00  | 5            |
  | 2  | Red Chair        | 50     | 2150.00 | 2            |
  | 3  | Disney Wardrobe  | 400    | 829.50  | 4            |
  | 4  | Executive Chair  | 17     | 9.90    | 3            |
  | 5  | Solar Panel      | 30     | 3000.25 | 4            |

#### Task:

Write an SQL query to display the name of products whose amount is between 10 and 20 and whose supplier's name starts with the letter 'P'.

#### SQL Query:

```sql
SELECT products.name AS "Product Name"
FROM products
JOIN providers ON products.id_providers = providers.id
WHERE products.amount BETWEEN 10 AND 20 AND providers.name LIKE 'P%';
```

#### Explanation of the Query:

- `SELECT products.name AS "Product Name"`: This line selects the `name` column from the `products` table, aliased as "Product Name" for clarity.

- `FROM products`: Specifies that the data is being selected from the `products` table.

- `JOIN providers ON products.id_providers = providers.id`: Joins the `products` table with the `providers` table where the provider IDs match.

- `WHERE products.amount BETWEEN 10 AND 20 AND providers.name LIKE 'P%'`: Filters the results to include only those products whose amount is between 10 and 20, and the name of their provider starts with the letter 'P'.

This query will help identify the products that meet the specified criteria.

#### Output Sample:

| Product Name    |
| --------------- |
| Executive Chair |

---

</details> 
<!-- ```end -->

### beecrowd SQL | 2622 - Legal Person

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The sales industry intends to run a promotion for all clients that are legal entities. The task is to display the names of the customers who are legal entities.

#### Schema:

1. **Table: `customers`**

   | Column       | Type                    |
   | ------------ | ----------------------- |
   | id (Primary Key) | numeric             |
   | name         | character varying (255) |
   | street       | character varying (255) |
   | city         | character varying (255) |
   | state        | char (2)                |
   | credit_limit | numeric                 |

2. **Table: `legal_person`**

   | Column          | Type         |
   | --------------- | ------------ |
   | id_customers (Foreign Key) | numeric  |
   | cnpj            | char (18)    |
   | contact         | character varying |

#### Sample Data:

- **customers:**

  | id | name                                   | street                           | city           | state | credit_limit |
  | -- | -------------------------------------- | -------------------------------- | -------------- | ----- | ------------ |
  | 1  | Nicolas Diogo Cardoso                  | Acesso Um                        | Porto Alegre   | RS    | 475          |
  | 2  | Cecília Olivia Rodrigues               | Rua Sizuka Usuy                  | Cianorte       | PR    | 3170         |
  | 3  | Augusto Fernando Carlos Eduardo Cardoso | Rua Baldomiro Koerich            | Palhoça        | SC    | 1067         |
  | 4  | Nicolas Diogo Cardoso                  | Acesso Um                        | Porto Alegre   | RS    | 475          |
  | 5  | Sabrina Heloisa Gabriela Barros        | Rua Engenheiro Tito Marques Fernandes | Porto Alegre | RS    | 4312        |
  | 6  | Joaquim Diego Lorenzo Araújo           | Rua Vitorino                     | Novo Hamburgo  | RS    | 2314         |

- **legal_person:**

  | id_customers | cnpj          | contact   |
  | ------------ | ------------- | --------- |
  | 4            | 85883842000191 | 99767-0562 |
  | 5            | 47773848000117 | 99100-8965  |

#### Task:

Write an SQL query to display the names of customers who are legal entities.

#### SQL Query:

```sql
SELECT customers.name AS "Customer Name"
FROM customers
JOIN legal_person ON customers.id = legal_person.id_customers;
```

#### Explanation of the Query:

- `SELECT customers.name AS "Customer Name"`: This line selects the `name` column from the `customers` table, aliased as "Customer Name" for clarity.

- `FROM customers`: Specifies that the data is being selected from the `customers` table.

- `JOIN legal_person ON customers.id = legal_person.id_customers`: Joins the `customers` table with the `legal_person` table where the customer IDs match those in the `legal_person` table.

This query will display the names of customers who are identified as legal entities in the database.

#### Output Sample:

| Customer Name                  |
| ------------------------------ |
| Nicolas Diogo Cardoso          |
| Sabrina Heloisa Gabriela Barros|

---

</details> 
<!-- ```end -->

### beecrowd SQL | 2623 - Categories with Various Products

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The sales industry requires a report to know what products are left in stock. The task is to display the product name and category name for products whose amount is greater than 100 and the category ID is 1, 2, 3, 6, or 9. The results should be shown in ascending order by category ID.

#### Schema:

1. **Table: `products`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |
   | amount | numeric               |
   | price  | numeric               |
   | id_categories (Foreign Key) | numeric  |

2. **Table: `categories`**

   | Column | Type                  |
   | ------ | --------------------- |
   | id (Primary Key) | numeric           |
   | name   | character varying (255) |

#### Sample Data:

- **products:**

  | id | name            | amount | price   | id_categories |
  | -- | --------------- | ------ | ------- | ------------- |
  | 1  | Blue Chair      | 30     | 300.00  | 9             |
  | 2  | Red Chair       | 200    | 2150.00 | 2             |
  | 3  | Disney Wardrobe | 400    | 829.50  | 4             |
  | 4  | Blue Toaster    | 20     | 9.90    | 3             |
  | 5  | Solar Panel     | 30     | 3000.25 | 4             |

- **categories:**

  | id | name        |
  | -- | ----------- |
  | 1  | Superior    |
  | 2  | Super Luxury|
  | 3  | Modern      |
  | 4  | Nerd        |
  | 5  | Infantile   |
  | 6  | Robust      |
  | 9  | Wood        |

#### Task:

Write an SQL query to display the product name and category name for products whose amount is greater than 100 and the category ID is 1, 2, 3, 6, or 9. Sort the results in ascending order by category ID.

#### SQL Query:

```sql
SELECT products.name AS "Product Name", categories.name AS "Category Name"
FROM products
JOIN categories ON products.id_categories = categories.id
WHERE products.amount > 100 AND products.id_categories IN (1, 2, 3, 6, 9)
ORDER BY products.id_categories ASC;
```

#### Explanation of the Query:

- `SELECT products.name AS "Product Name", categories.name AS "Category Name"`: This line selects the `name` column from both `products` and `categories` tables, aliased for clarity.

- `FROM products`: Specifies that the data is being selected from the `products` table.

- `JOIN categories ON products.id_categories = categories.id`: Joins the `products` table with the `categories` table where the category IDs match.

- `WHERE products.amount > 100 AND products.id_categories IN (1, 2, 3, 6, 9)`: Filters the results to include only those products whose amount is greater than 100 and whose category ID is among 1, 2, 3, 6, or 9.

- `ORDER BY products.id_categories ASC`: Orders the results in ascending order based on the category ID.

This query will help identify the products that meet the specified criteria, sorted by category.

#### Output Sample:

| Product Name | Category Name  |
| ------------ | -------------- |
| Red Chair    | Super Luxury   |

---

</details> 
<!-- ```end -->

### beecrowd SQL | 2624 - Number of Cities per Customers

<details>

<summary>Click Here</summary>

**Author:** Paulo R. Rodegheri, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The company board requires a report on how many distinct cities the company has reached. The task is to display the number of distinct cities in the customers table.

#### Schema:

**Table: `customers`**

| Column       | Type                    |
| ------------ | ----------------------- |
| id (Primary Key) | numeric             |
| name         | character varying (255) |
| street       | character varying (255) |
| city         | character varying (255) |
| state        | char (2)                |
| credit_limit | numeric                 |

#### Sample Data:

**customers:**

| id | name                                    | street                           | city           | state | credit_limit |
| -- | --------------------------------------- | -------------------------------- | -------------- | ----- | ------------ |
| 1  | Nicolas Diogo Cardoso                   | Acesso Um                        | Porto Alegre   | RS    | 475          |
| 2  | Cecília Olivia Rodrigues                | Rua Sizuka Usuy                  | Cianorte       | PR    | 3170         |
| 3  | Augusto Fernando Carlos Eduardo Cardoso | Rua Baldomiro Koerich            | Palhoça        | SC    | 1067         |
| 4  | Nicolas Diogo Cardoso                   | Acesso Um                        | Porto Alegre   | RS    | 475          |
| 5  | Sabrina Heloisa Gabriela Barros         | Rua Engenheiro Tito Marques Fernandes | Porto Alegre | RS    | 4312        |
| 6  | Joaquim Diego Lorenzo Araújo            | Rua Vitorino                     | Novo Hamburgo  | RS    | 2314         |

#### Task:

Write an SQL query to display the number of distinct cities in the customers table.

#### SQL Query:

```sql
SELECT COUNT(DISTINCT city) AS "Number of Cities"
FROM customers;
```

#### Explanation of the Query:

- `SELECT COUNT(DISTINCT city) AS "Number of Cities"`: This line selects and counts the distinct `city` values from the `customers` table. The result is aliased as "Number of Cities" for clarity.

This query will provide the total count of distinct cities where the company's customers are located.

#### Output Sample:

| Number of Cities |
| ---------------- |
| 4                |

---

</details> 
<!-- ```end -->

### beecrowd SQL | 2625 - CPF Validation

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The communications managers require a report on the natural person customer data with validated CPFs. The task is to select all CPFs of customers and apply a mask to the data, formatting it as '000.000.000-00'.

#### Schema:

1. **Table: `customers`**

   | Column       | Type                    |
   | ------------ | ----------------------- |
   | id (Primary Key) | numeric             |
   | name         | character varying (255) |
   | street       | character varying (255) |
   | city         | character varying (255) |
   | state        | char (2)                |
   | credit_limit | numeric                 |

2. **Table: `natural_person`**

   | Column          | Type         |
   | --------------- | ------------ |
   | id_customers (Foreign Key) | numeric  |
   | cpf            | char (14)    |

#### Sample Data:

- **customers:**

  | id | name                                    | street                           | city           | state | credit_limit |
  | -- | --------------------------------------- | -------------------------------- | -------------- | ----- | ------------ |
  | 1  | Nicolas Diogo Cardoso                   | Acesso Um                        | Porto Alegre   | RS    | 475          |
  | 2  | Cecília Olivia Rodrigues                | Rua Sizuka Usuy                  | Cianorte       | PR    | 3170         |
  | ... | ...                                    | ...                              | ...            | ...   | ...          |

- **natural_person:**

  | id_customers | cpf        |
  | ------------ | ---------- |
  | 1            | 26774287840 |
  | 2            | 97918477200  |

#### Task:

Write an SQL query to select all CPFs of customers and apply a mask to format them as '000.000.000-00'.

#### SQL Query:

```sql
SELECT FORMAT(cpf, '###.###.###-##') AS "CPF"
FROM natural_person;
```

#### Explanation of the Query:

- `SELECT FORMAT(cpf, '###.###.###-##') AS "CPF"`: This line selects the `cpf` column from the `natural_person` table and applies a mask to format the CPF numbers in the desired format. The result is aliased as "CPF" for clarity.

This query will format and display all customer CPFs according to the specified mask.

#### Output Sample:

| CPF             |
| --------------- |
| 267.742.878-40  |
| 979.184.772-00  |

---

</details> 
<!-- ```end -->

Note: The SQL function used in the query (`FORMAT`) might vary depending on the SQL database system used (e.g., MySQL, PostgreSQL, etc.). The given query is a general representation, and the exact function name and syntax might need adjustments based on the specific SQL database in use.

### beecrowd SQL | 2737 - Lawyers

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The manager of Mangojata Lawyers requires a report on their current lawyers. The report should include the name of the lawyer with the most clients, the one with the fewest clients, and the average number of clients considering all lawyers. The average must be presented as an integer.

#### Schema:

**Table: `lawyers`**

| Column          | Type     |
| --------------- | -------- |
| register (Primary Key) | integer |
| name            | varchar  |
| customers_number| integer  |

#### Sample Data:

**lawyers:**

| register | name              | customers_number |
| -------- | ----------------- | ---------------- |
| 1648     | Marty M. Harrison | 5                |
| 2427     | Jonathan J. Blevins | 15             |
| 3365     | Chelsey D. Sanders | 20               |
| 4153     | Dorothy W. Ford   | 16               |
| 5525     | Penny J. Cormier  | 6                |

#### Task:

Write an SQL query to show the name of the lawyer with the most clients, the one with the fewest clients, and the average number of clients considering all lawyers.

#### SQL Query:

```sql
SELECT name, customers_number
FROM lawyers
ORDER BY customers_number DESC
LIMIT 1
UNION ALL
SELECT name, customers_number
FROM lawyers
ORDER BY customers_number ASC
LIMIT 1
UNION ALL
SELECT 'Average' AS name, CAST(AVG(customers_number) AS INTEGER) AS customers_number
FROM lawyers;
```

#### Explanation of the Query:

- The first `SELECT` statement finds the lawyer with the most clients by ordering in descending order and limiting to 1 result.
- The second `SELECT` statement finds the lawyer with the fewest clients by ordering in ascending order and limiting to 1 result.
- The third `SELECT` statement calculates the average number of clients for all lawyers and casts it as an integer. It uses 'Average' as a placeholder name for clarity in the output.

This query will provide the required information in the specified format, helping the manager get insights into the distribution of clients among the lawyers.

#### Output Sample:

| name              | customers_number |
| ----------------- | ---------------- |
| Chelsey D. Sanders | 20               |
| Marty M. Harrison | 5                |
| Average           | 12               |

---

</details> 
<!-- ```end -->

Note: The SQL query is structured to work with most SQL database systems. However, minor adjustments might be necessary depending on the specific SQL dialect used (e.g., MySQL, PostgreSQL, etc.).

### beecrowd SQL | 2738 - Contest

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

Mars Technology University has Open Positions for researchers. You are tasked with presenting a list of candidates, showing each candidate's name and final score (with two decimal places of precision). The list should be ordered by score, highest first. The score is calculated as a weighted average: 

\[ \text{Avg} = \frac{(\text{math} \times 2) + (\text{specific} \times 3) + (\text{project\_plan} \times 5)}{10} \]

#### Schema:

1. **Table: `candidate`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | integer |
   | name   | varchar |

2. **Table: `score`**

   | Column | Type    |
   | ------ | ------- |
   | candidate_id (Foreign Key) | integer |
   | math | numeric |
   | specific | numeric |
   | project_plan | numeric |

#### Sample Data:

- **candidate:**

  | id | name                     |
  | -- | ------------------------ |
  | 1  | Michael P Cannon         |
  | 2  | Barbra J Cable           |
  | 3  | Ronald D Jones           |
  | 4  | Timothy K Fitzsimmons    |
  | 5  | Ivory B Morrison         |
  | 6  | Sheila R Denis           |
  | 7  | Edward C Durgan          |
  | 8  | William K Spencer        |
  | 9  | Donna D Pursley          |
  | 10 | Ann C Davis              |

- **score:**

  | candidate_id | math | specific | project_plan |
  | ------------ | ---- | -------- | ------------ |
  | 1            | 76   | 58       | 21           |
  | 2            | 4    | 5        | 22           |
  | 3            | 15   | 59       | 12           |
  | 4            | 41   | 42       | 99           |
  | 5            | 22   | 90       | 9            |
  | 6            | 82   | 77       | 15           |
  | 7            | 82   | 99       | 56           |
  | 8            | 11   | 4        | 22           |
  | 9            | 16   | 29       | 94           |
  | 10           | 1    | 7        | 59           |

#### Task:

Write an SQL query to present the candidate list with names and final scores, ordered by score (highest first). The final score should be displayed with two decimal places.

#### SQL Query:

```sql
SELECT candidate.name, ROUND(((score.math * 2) + (score.specific * 3) + (score.project_plan * 5)) / 10, 2) AS avg
FROM candidate
JOIN score ON candidate.id = score.candidate_id
ORDER BY avg DESC;
```

#### Explanation of the Query:

- The `SELECT` statement calculates the weighted average for each candidate using the given formula and rounds it to two decimal places. It also selects the candidate's name.
- The `FROM` and `JOIN` statements combine the `candidate` and `score` tables based on the candidate's ID.
- The `ORDER BY` clause orders the results by the calculated average score in descending order.

This query will provide the list of candidates with their final scores, helping in the evaluation process for the open researcher positions.

#### Output Sample:

| name                  | avg   |
| --------------------- | ----- |
| Edward C Durgan       | 74.10 |
| Timothy K Fitzsimmons | 70.30 |
| Donna D Pursley       | 58.90 |
| Sheila R Denis        | 47.00 |
| Michael P Cannon      | 43.10 |
| Ivory B Morrison      | 35.90 |
| Ann C Davis           | 31.80 |
| Ronald D Jones        | 26.70 |
| William K Spencer     | 14.40 |
| Barbra J Cable        | 13.30 |

---

</details> 
<!-- ```end -->

Note: The SQL function `ROUND` used in the query might have different syntax or usage based on the SQL database system (e.g., MySQL, PostgreSQL, etc.). The query provided is a general example, and minor adjustments may be required depending on the specific SQL dialect used.

### beecrowd SQL | 2739 - Payday

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The Central Bank of Financing needs assistance in recovering the collection dates for loan parcels after a server failure. The task is to select the names of clients and the day of the month on which each client must pay their parcel. The day of the month must be presented as an integer.

#### Schema:

**Table: `loan`**

| Column | Type            |
| ------ | --------------- |
| id (Primary Key) | integer     |
| name   | varchar         |
| value  | numeric         |
| payday | timestamp (ISO YMD) |

#### Sample Data:

**loan:**

| id | name               | value   | payday     |
| -- | ------------------ | ------- | ---------- |
| 1  | Cristian Ghyprievy | 3000.50 | 2017-10-19 |
| 2  | John Serial        | 10000   | 2017-10-10 |
| 3  | Michael Seven      | 5000.40 | 2017-10-17 |
| 4  | Joana Cabel        | 2000    | 2017-10-05 |
| 5  | Miguel Santos      | 4050    | 2017-10-20 |

#### Task:

Write an SQL query to select the names of clients and the day of the month when each client must pay their parcel.

#### SQL Query:

```sql
SELECT name, EXTRACT(DAY FROM payday) AS day
FROM loan;
```

#### Explanation of the Query:

- `SELECT name, EXTRACT(DAY FROM payday) AS day`: This line selects the `name` column from the `loan` table and extracts the day part of the `payday` timestamp. The day is aliased as "day" for clarity in the output.

This query will provide the names of clients and the specific days of the month when they need to make their loan payments.

#### Output Sample:

| name               | day |
| ------------------ | --- |
| Cristian Ghyprievy | 19  |
| John Serial        | 10  |
| Michael Seven      | 17  |
| Joana Cabel        | 5   |
| Miguel Santos      | 20  |

---

</details> 
<!-- ```end -->

Note: The SQL function `EXTRACT` is used to retrieve specific parts of a date or time in SQL. The exact syntax may vary slightly depending on the SQL database system being used (e.g., MySQL, PostgreSQL, etc.). The query provided is a general representation, and slight adjustments might be necessary for specific SQL dialects.

### beecrowd SQL | 2740 - League

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The International Underground Excavation League needs assistance in organizing their event results. The task is to select the top three teams with the prefix "Podium: " and the last two teams, indicating demotion, with the prefix "Demoted:".

#### Schema:

**Table: `league`**

| Column    | Type    |
| --------- | ------- |
| position (Primary Key) | integer |
| team      | varchar |

#### Sample Data:

**league:**

| position | team                   |
| -------- | ---------------------- |
| 1        | The Quack Bats         |
| 2        | The Responsible Hornets|
| 3        | The Bawdy Dolphins     |
| ...      | ...                    |
| 14       | The Rough Robins       |
| 15       | The Silver Crocs       |

#### Task:

Write an SQL query to select the first three teams as "Podium" and the last two teams as "Demoted".

#### SQL Query:

```sql
(SELECT 'Podium: ' || team AS name FROM league ORDER BY position ASC LIMIT 3)
UNION ALL
(SELECT 'Demoted: ' || team AS name FROM league ORDER BY position DESC LIMIT 2);
```

#### Explanation of the Query:

- The first `SELECT` statement selects the top three teams (by ascending order of position) and concatenates their names with "Podium: ".
- The second `SELECT` statement selects the last two teams (by descending order of position) and concatenates their names with "Demoted: ".
- The `UNION ALL` combines the results of these two queries.

This query effectively identifies the top performers and those facing demotion, as per the league's structure.

#### Output Sample:

| name                         |
| ---------------------------- |
| Podium: The Quack Bats       |
| Podium: The Responsible Hornets |
| Podium: The Bawdy Dolphins   |
| Demoted: The Rough Robins    |
| Demoted: The Silver Crocs    |

---

</details> 
<!-- ```end -->

Note: The SQL syntax used for concatenation (`||`) might vary depending on the SQL database system (e.g., MySQL uses `CONCAT`). The provided query is a general example, and adjustments may be necessary depending on the specific SQL dialect used.

### beecrowd SQL | 2741 - Students Grades

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

At South Transylvania University, the semester has ended, and the list of approved students for Alchemy 104 needs to be published. The task is to show the word 'Approved: ' alongside the name and grade of students who have been approved (grade ≥7). The list should be sorted by grade, with higher grades first.

#### Schema:

**Table: `students`**

| Column | Type    |
| ------ | ------- |
| id (Primary Key) | integer |
| name   | varchar |
| grade  | numeric |

#### Sample Data:

**students:**

| id | name            | grade |
| -- | --------------- | ----- |
| 1  | Terry B. Padilla | 7.3   |
| 2  | William S. Ray   | 0.6   |
| 3  | Barbara A. Gongora | 5.2 |
| 4  | Julie B. Manzer  | 6.7   |
| 5  | Teresa J. Axtell | 4.6   |
| 6  | Ben M. Dantzler  | 9.6   |

#### Task:

Write an SQL query to display the names and grades of students who have been approved, prefixed with 'Approved: '. The list should be sorted by grade in descending order.

#### SQL Query:

```sql
SELECT 'Approved: ' || name AS name, grade
FROM students
WHERE grade >= 7
ORDER BY grade DESC;
```

#### Explanation of the Query:

- `SELECT 'Approved: ' || name AS name, grade`: This line selects the `name` column from the `students` table, prefixes it with 'Approved: ', and selects the `grade` column.
- `FROM students`: Specifies that the data is being selected from the `students` table.
- `WHERE grade >= 7`: Filters the results to include only students with a grade of 7 or higher.
- `ORDER BY grade DESC`: Orders the results by the `grade` column in descending order.

This query will display the names and grades of students who have been approved, in order of their grades.

#### Output Sample:

| name                        | grade |
| --------------------------- | ----- |
| Approved: Ben M. Dantzler   | 9.6   |
| Approved: Terry B. Padilla  | 7.3   |

---

</details> 
<!-- ```end -->

Note: The SQL syntax for concatenation (`||`) may differ based on the SQL database system used. The provided query is a general example and may require adjustments depending on the specific SQL dialect.

### beecrowd SQL | 2742 - Richard's Multiverse

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

Richard, a scientist known for his multiverse theory, needs assistance in analyzing data about parallel universes. The task is to select every "Richard" from dimensions C875 and C774, along with their existence probability (the famous factor N), calculated to three decimal places. The N factor is computed by multiplying the omega value by 1.618. The data should be sorted by the least omega value.

#### Schema:

1. **Table: `dimensions`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |

2. **Table: `life_registry`**

   | Column | Type    |
   | ------ | ------- |
   | id (Primary Key) | numeric |
   | name   | varchar |
   | omega  | numeric |
   | dimensions_id (Foreign Key) | numeric |

#### Sample Data:

- **dimensions:**

  | id | name |
  | -- | ---- |
  | 1  | C774 |
  | 2  | C784 |
  | ...| ...  |
  | 5  | C875 |

- **life_registry:**

  | id | name                | omega | dimensions_id |
  | -- | ------------------- | ----- | ------------- |
  | 1  | Richard Postman     | 5.6   | 2             |
  | 2  | Simple Jelly        | 1.4   | 1             |
  | 3  | Richard Gran Master | 2.5   | 1             |
  | ...| ...                 | ...   | ...           |

#### Task:

Write an SQL query to select every "Richard" from dimensions C875 and C774, along with the N factor (omega × 1.618), sorted by the least omega value.

#### SQL Query:

```sql
SELECT life_registry.name, ROUND(life_registry.omega * 1.618, 3) AS "The N Factor"
FROM life_registry
JOIN dimensions ON life_registry.dimensions_id = dimensions.id
WHERE dimensions.name IN ('C875', 'C774') AND life_registry.name LIKE 'Richard%'
ORDER BY life_registry.omega;
```

#### Explanation of the Query:

- The `SELECT` statement chooses the `name` from `life_registry` and calculates the N factor as `omega * 1.618`, rounding to three decimal places.
- The `FROM` and `JOIN` statements combine the `life_registry` and `dimensions` tables based on the `dimensions_id`.
- The `WHERE` clause filters for dimensions C875 and C774 and names starting with 'Richard'.
- The `ORDER BY` clause sorts the results by the omega value in ascending order.

This query will display the required Richards from the specified dimensions alongside their calculated N factor.

#### Output Sample:

| name                | The N Factor |
| ------------------- | ------------ |
| Richard Gran Master | 4.045        |

---

</details> 
<!-- ```end -->

Note: The SQL function `ROUND` used in the query might have different syntax or usage based on the SQL database system (e.g., MySQL, PostgreSQL, etc.). The provided query is a general representation, and slight adjustments may be required for specific SQL dialects.

### beecrowd SQL | 2743 - Number of Characters

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

The Global Organization of Characters at People’s Names (GOCPN) conducted a census to determine the number of characters in people's names. The task is to show the number of characters for each name, sorted in decreasing order of the number of characters.

#### Schema:

**Table: `people`**

| Column | Type    |
| ------ | ------- |
| id (Primary Key) | integer |
| name   | varchar |

#### Sample Data:

**people:**

| id | name      |
| -- | --------- |
| 1  | Karen     |
| 2  | Manuel    |
| 3  | Ygor      |
| 4  | Valentine |
| 5  | Jo        |

#### Task:

Write an SQL query to display the number of characters in each name, sorted by the decreasing number of characters.

#### SQL Query:

```sql
SELECT name, LENGTH(name) AS length
FROM people
ORDER BY length DESC;
```

#### Explanation of the Query:

- `SELECT name, LENGTH(name) AS length`: This line selects the `name` column from the `people` table and calculates the length of each name using the `LENGTH` function. The result is aliased as "length" for clarity.
- `FROM people`: Specifies that the data is being selected from the `people` table.
- `ORDER BY length DESC`: Orders the results by the calculated length in descending order.

This query will display the names and their corresponding character count, sorted by the length of the names in descending order.

#### Output Sample:

| name       | length |
| ---------- | ------ |
| Valentine  | 9      |
| Manuel     | 6      |
| Karen      | 5      |
| Ygor       | 4      |
| Jo         | 2      |

---

</details> 
<!-- ```end -->

Note: The SQL function `LENGTH` is used to calculate the number of characters in a string. The exact syntax and name of this function might vary depending on the SQL database system (e.g., `LEN` in some systems). The provided query is a general representation, and minor adjustments may be necessary for specific SQL dialects.

### beecrowd SQL | 2744 - Passwords

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

As a consultant for a company, you've noticed that passwords are stored as plain text, which is a significant security risk. The task is to convert every password to the MD5 format and display the client id, the original password, and the new MD5 hash.

#### Schema:

**Table: `account`**

| Column | Type    |
| ------ | ------- |
| id (Primary Key) | integer |
| name   | varchar |
| login  | varchar |
| password | varchar |

#### Sample Data:

**account:**

| id | name              | login      | password    |
| -- | ----------------- | ---------- | ----------- |
| 1  | Joyce P. Parry    | Promeraw   | noh1Oozei   |
| 2  | Michael T. Gonzalez | Phers1942 | Iath3see9bi |
| 3  | Heather W. Lawless | Hankicht  | diShono4    |
| 4  | Otis C. Hitt      | Conalothe  | zooFohH7w   |
| 5  | Roger N. Brownfield | Worseente | fah7ohNg   |

#### Task:

Write an SQL query to convert passwords into MD5 format and display the client id, the original password, and the new MD5 hash.

#### SQL Query:

```sql
SELECT id, password, MD5(password) AS MD5
FROM account;
```

#### Explanation of the Query:

- `SELECT id, password, MD5(password) AS MD5`: This line selects the `id` and `password` from the `account` table and also generates an MD5 hash of the password. The MD5 hash is aliased as "MD5" for clarity.
- `FROM account`: Specifies that the data is being selected from the `account` table.

This query will display the client id, the original password, and its corresponding MD5 hash, thereby enhancing the security of password storage.

#### Output Sample:

| id | password    | MD5                                |
| -- | ----------- | ---------------------------------- |
| 1  | noh1Oozei   | b67ed42ced0e0a19ce7ed904bb94b607   |
| 2  | Iath3see9bi | 66877b2da87fb09af3f5602f31c6d35c   |
| 3  | diShono4    | d19c9be4c00c683a4688948b81eb2a1d   |
| 4  | zooFohH7w   | 202b76ed4a556fdbf409505a8023695e   |
| 5  | fah7ohNg    | 05b3dccaa70f228f1bedc7a285e50d9d   |

---

</details> 
<!-- ```end -->

Note: The MD5 function is commonly used in SQL for generating hash values from strings. However, it's important to mention that MD5 is no longer considered secure for cryptographic purposes in real-world applications, and more secure hashing algorithms like SHA-256 are recommended.

### beecrowd SQL | 2745 - Taxes

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

You are preparing for the International Personal Tax meeting with a proposal: individuals with an income higher than 3000 must pay a tax to the government, equal to 10% of their income. Your task is to show the name and the tax value of each person who earns more than 3000, with two decimal places of precision.

#### Schema:

**Table: `people`**

| Column | Type    |
| ------ | ------- |
| id (Primary Key) | integer |
| name   | varchar |
| salary | numeric |

#### Sample Data:

**people:**

| id | name              | salary |
| -- | ----------------- | ------ |
| 1  | James M. Tabarez  | 883    |
| 2  | Rafael T. Hendon  | 4281   |
| 3  | Linda J. Gardner  | 4437   |
| 4  | Nicholas J. Conn  | 8011   |
| 5  | Karol A. Morales  | 2508   |
| 6  | Lolita S. Graves  | 8709   |

#### Task:

Write an SQL query to display the name and the tax value (10% of salary) for each person whose salary is more than 3000. The tax value should be shown with two decimal places.

#### SQL Query:

```sql
SELECT name, ROUND(salary * 0.10, 2) AS tax
FROM people
WHERE salary > 3000;
```

#### Explanation of the Query:

- `SELECT name, ROUND(salary * 0.10, 2) AS tax`: This line selects the `name` column from the `people` table and calculates the tax value as 10% of the salary, rounding it to two decimal places. The result is aliased as "tax" for clarity.
- `FROM people`: Specifies that the data is being selected from the `people` table.
- `WHERE salary > 3000`: Filters the results to include only individuals with a salary greater than 3000.

This query will display the names and calculated tax values for individuals with high incomes.

#### Output Sample:

| name              | tax    |
| ----------------- | ------ |
| Rafael T. Hendon  | 428.10 |
| Linda J. Gardner  | 443.70 |
| Nicholas J. Conn  | 801.10 |
| Lolita S. Graves  | 870.90 |

---

</details> 
<!-- ```end -->

Note: The SQL function `ROUND` is used to round numeric values to a specified number of decimal places. The exact syntax and behavior might vary slightly depending on the SQL database system being used (e.g., MySQL, PostgreSQL, etc.). The provided query is a general representation, and minor adjustments may be required for specific SQL dialects.

### beecrowd SQL | 2746 - Viruses

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

In recent virus research, it has been discovered that replacing the protein H1 (Hemagglutinin) with the X protein (Xenomorphina) has significant effects against viral diseases. Your task is to replace every occurrence of the string “H1” with 'X' in the virus database.

#### Schema:

**Table: `virus`**

| Column | Type    |
| ------ | ------- |
| id (Primary Key) | integer |
| name   | varchar |

#### Sample Data:

**virus:**

| id | name  |
| -- | ----- |
| 1  | H1RT  |
| 2  | H7H1  |
| 3  | HUN8  |
| 4  | XH1HX |
| 5  | XXXX  |

#### Task:

Write an SQL query to replace every occurrence of “H1” with 'X' in the names of viruses.

#### SQL Query:

```sql
SELECT REPLACE(name, 'H1', 'X') AS name
FROM virus;
```

#### Explanation of the Query:

- `SELECT REPLACE(name, 'H1', 'X') AS name`: This line uses the `REPLACE` function to change every occurrence of 'H1' to 'X' in the `name` column of the `virus` table. The result is aliased as "name" for clarity.
- `FROM virus`: Specifies that the data is being selected from the `virus` table.

This query will display the updated names of the viruses with the 'H1' protein replaced by 'X'.

#### Output Sample:

| name |
| ---- |
| XRT  |
| H7X  |
| HUN8 |
| XXHX |
| XXXX |

---

</details> 
<!-- ```end -->

Note: The SQL function `REPLACE` is used to replace occurrences of a specified string with another string. The syntax and behavior of this function are generally consistent across different SQL database systems (e.g., MySQL, PostgreSQL, etc.). The provided query is a standard representation, and it should work in most SQL environments.

### beecrowd SQL | 2746 - Viruses

<details>

<summary>Click Here</summary>

**Author:** Marcos Lima, BR Brazil

**Time Limit:** 1 second

**Memory Limit:** 200 MB

---

#### Problem Description:

Viruses are evolving, and a recent discovery shows that replacing the H1 protein with Xenomorphina (X) has significant effects against viral diseases. You need to update the virus database to reflect this change by replacing every instance of "H1" with 'X'.

#### Schema:

**Table: `virus`**

| Column | Type    |
| ------ | ------- |
| id (Primary Key) | integer |
| name   | varchar |

#### Sample Data:

**virus:**

| id | name  |
| -- | ----- |
| 1  | H1RT  |
| 2  | H7H1  |
| 3  | HUN8  |
| 4  | XH1HX |
| 5  | XXXX  |

#### Task:

Write an SQL query to replace every occurrence of “H1” with 'X' in the names of viruses.

#### SQL Query:

```sql
SELECT REPLACE(name, 'H1', 'X') AS name
FROM virus;
```

#### Explanation of the Query:

- `SELECT REPLACE(name, 'H1', 'X') AS name`: This line uses the `REPLACE` function to change every occurrence of 'H1' to 'X' in the `name` column of the `virus` table. The result is aliased as "name" for clarity.
- `FROM virus`: Specifies that the data is being selected from the `virus` table.

This query will display the updated names of the viruses with the 'H1' protein replaced by 'X'.

#### Output Sample:

| name |
| ---- |
| XRT  |
| H7X  |
| HUN8 |
| XXHX |
| XXXX |

---

</details> 
<!-- ```end -->

Note: The SQL function `REPLACE` is used to replace occurrences of a specified string with another string. The syntax and behavior of this function are generally consistent across different SQL database systems (e.g., MySQL, PostgreSQL, etc.). The provided query is a standard representation, and it should work in most SQL environments.

<!-- 2989 have some issue -->
<!-- 2990 have some issue -->
<!-- 2991 have some issue -->