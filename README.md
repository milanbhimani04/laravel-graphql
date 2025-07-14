# 🚀 Laravel GraphQL API with Lighthouse

This project is a basic **GraphQL API** built using **Laravel** and the **Lighthouse** GraphQL server package. It includes CRUD operations for a `User` model and uses the GraphQL Playground (via GraphiQL) for testing queries and mutations.

> ✅ Inspired by: [milanbhimani04/laravel-graphql](https://github.com/milanbhimani04/laravel-graphql)

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/laravel-graphql.git
cd laravel-graphql

composer install
cp .env.example .env
php artisan key:generate

# Create new Laravel project
laravel new laravel-graphql

# Install Lighthouse GraphQL
composer require nuwave/lighthouse

# Publish the default GraphQL schema
php artisan vendor:publish --tag=lighthouse-schema

# Publish the Lighthouse config file
php artisan vendor:publish --tag=lighthouse-config

# Optional: Install GraphiQL Playground for testing
composer require mll-lab/laravel-graphiql

php artisan migrate:fresh

php artisan serve
