# Product CRUD Operations with Mongoose

## Experiment Aim
To perform CRUD operations for a product database using Mongoose.

## Objectives
- Build a REST API using Node.js and Express.
- Connect to MongoDB Atlas using Mongoose.
- Implement full CRUD operations for products.
- Validate required fields and price constraints.
- Deploy the API online using Vercel.

## Technology Stack
- Node.js 18+
- Express.js
- MongoDB Atlas
- Mongoose
- Postman
- Vercel

## Project Structure
```
product-crud-mongoose/
  server.js
  config/db.js
  models/Product.js
  controllers/productController.js
  routes/productRoutes.js
  package.json
  vercel.json
  README.md
```

## API Documentation
Base URL (local): `http://localhost:5000`

### 1) Create Product
- Method: `POST`
- Endpoint: `/api/products`
- Body:
```json
{
  "name": "Wireless Mouse",
  "price": 29.99,
  "category": "Electronics",
  "inStock": true
}
```

### 2) Get All Products
- Method: `GET`
- Endpoint: `/api/products`

### 3) Get Product by ID
- Method: `GET`
- Endpoint: `/api/products/:id`

### 4) Update Product
- Method: `PUT`
- Endpoint: `/api/products/:id`

### 5) Delete Product
- Method: `DELETE`
- Endpoint: `/api/products/:id`

## Validation Rules
- `name` is required.
- `price` is required and must be a positive number.

## Installation Steps
1. Clone the repository.
2. Run dependencies install:
```bash
npm install
```
3. Create `.env` from `.env.example` and set your MongoDB Atlas URI.
4. Start the server:
```bash
node server.js
```

## MongoDB Setup (Atlas)
1. Create a cluster in MongoDB Atlas.
2. Create a database user and whitelist your IP (`0.0.0.0/0` for testing).
3. Get your connection string and set:

```env
MONGO_URI=your_mongodb_atlas_connection_string
```

## Deployment
- Platform: Vercel
- Add environment variable `MONGO_URI` in Vercel project settings.

Deployment link: `https://product-crud-mongoose-api.vercel.app`

## Expected Output Example
```json
{
  "_id": "65f4a8b7c1e6a8c1f4b8c7d1",
  "name": "Wireless Mouse",
  "price": 29.99,
  "category": "Electronics",
  "inStock": true,
  "createdAt": "2024-03-15T10:30:00.000Z",
  "__v": 0
}
```

## Postman Example
- Request: `POST {{baseUrl}}/api/products`
- Headers: `Content-Type: application/json`
- Body:
```json
{
  "name": "Wireless Mouse",
  "price": 29.99,
  "category": "Electronics",
  "inStock": true
}
```

