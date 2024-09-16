# E-Commerce Back End

## Description

This is the back-end for an e-commerce site, designed to manage a product catalog, including categories, tags, and product listings. The application uses Express.js as the server framework, Sequelize as the ORM (Object-Relational Mapping) tool, and PostgreSQL as the database. This project provides a RESTful API for handling CRUD operations on products, categories, and tags.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Routes](#routes)
- [Testing API Endpoints with Insomnia](#testing-api-endpoints-with-insomnia)
- [Technologies](#technologies)
- [License](#license)

## Installation

1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Navigate to the project directory:
    ```bash
    cd e-commerce-back-end
    ```
3. Install the dependencies:
    ```bash
    npm install
    ```
4. Create a `.env` file and configure the following environment variables:
    ```bash
    DB_NAME='your_database_name'
    DB_USER='your_database_username'
    DB_PASSWORD='your_database_password'
    DB_HOST='localhost'
    DB_PORT=5432
    ```
5. Initialize the database:
    ```bash
    npx sequelize-cli db:create
    npx sequelize-cli db:migrate
    ```
6. Seed the database (optional for testing):
    ```bash
    npm run seed
    ```
7. Start the server:
    ```bash
    npm start
    ```

## Usage

This project provides API endpoints to manage products, categories, and tags. You can interact with these endpoints through a tool like Insomnia or Postman to test the back-end functionality.

## Routes

### Category Routes

- **GET** `/api/categories`: Retrieves all categories.
- **GET** `/api/categories/:id`: Retrieves a category by its ID.
- **POST** `/api/categories`: Creates a new category.
- **PUT** `/api/categories/:id`: Updates an existing category by ID.
- **DELETE** `/api/categories/:id`: Deletes a category by ID.

### Product Routes

- **GET** `/api/products`: Retrieves all products.
- **GET** `/api/products/:id`: Retrieves a product by its ID.
- **POST** `/api/products`: Creates a new product.
- **PUT** `/api/products/:id`: Updates an existing product by ID.
- **DELETE** `/api/products/:id`: Deletes a product by ID.

### Tag Routes

- **GET** `/api/tags`: Retrieves all tags.
- **GET** `/api/tags/:id`: Retrieves a tag by its ID.
- **POST** `/api/tags`: Creates a new tag.
- **PUT** `/api/tags/:id`: Updates an existing tag by ID.
- **DELETE** `/api/tags/:id`: Deletes a tag by ID.

## Testing API Endpoints with Insomnia

1. Install Insomnia or any API client.
2. Make sure your server is running by executing:
    ```bash
    npm start
    ```
3. In Insomnia, create requests for the different routes.

- Example to retrieve all categories:
    - Method: **GET**
    - URL: `http://localhost:3001/api/categories`
  
- Example to create a new product:
    - Method: **POST**
    - URL: `http://localhost:3001/api/products`
    - Body:
      ```json
      {
        "product_name": "New Product",
        "price": 29.99,
        "stock": 10,
        "category_id": 1,
        "tagIds": [1, 2]
      }
      ```

## Technologies

- Node.js
- Express.js
- Sequelize
- PostgreSQL
- dotenv
- Bcrypt
- Express-session

## License

This project is licensed under the MIT License.

## WATCH HOW TO VIDEO
(https://vimeo.com/1010044694)