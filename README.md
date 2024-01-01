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

