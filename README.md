# Laravel Sanctum REST API with Bearer Token Authentication

This is a simple REST API built using Laravel Sanctum that provides basic CRUD (Create, Read, Update, Delete) functionality for blog posts. It includes bearer token authentication for secure access.

## Requirements

- PHP >= 7.3
- Laravel >= 7.x
- Composer

## Installation

1. Clone the repository and navigate to the project root.

2. Install the dependencies.

> composer install


3. Set up the database by creating a new `.env` file and updating the database credentials.

> cp .env.example .env <br>  
> php artisan key:generate <br>  
> php artisan migrate

4. Start the server.


## Usage

1. Register a new user by sending a `POST` request to `/api/register` with the following JSON data:

```json
{
"name": "John Doe",
"email": "johndoe@example.com",
"password": "password123"
}
```

2. Log in to receive a bearer token by sending a `POST` request to `/api/login` with the following JSON data:

```json
{
"email": "johndoe@example.com",
"password": "password123"
}
```

3. Use the bearer token to access protected routes by including it in the `Authorization` header of your requests:

> Authorization: Bearer <token>


4. Perform CRUD operations on blog posts by sending requests to the following endpoints:

- `GET /api/posts` to retrieve all posts
- `GET /api/posts/{id}` to retrieve a specific post
- `POST /api/posts` to create a new post
- `PUT /api/posts/{id}` to update an existing post
- `DELETE /api/posts/{id}` to delete a post

> Include the necessary JSON data in the body of your requests as appropriate.


