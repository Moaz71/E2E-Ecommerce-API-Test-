
# 🛒 E2E Ecommerce API Testing Project

This project contains automated API test cases for an end-to-end Ecommerce system using Postman. The collection covers the major user flows such as login, product creation, order placement, and cleanup.

## 📁 Project Structure

- **Postman Collection**: `E2E Ecommerce API Test.postman_collection.json`
- **Environment File**: `E2E Ecommerce Env.postman_environment.json`

## 🌐 Base URL
```
https://rahulshettyacademy.com/api/ecom
```

## 🔄 Workflow Covered

The following flow simulates a full e-commerce transaction lifecycle:

1. **Login** (`/auth/login`)
   - Authenticates user.
   - Stores `token` and `userId` in environment.

2. **Create Product** (`/product/add-product`)
   - Adds a product to the system using `multipart/form-data`.
   - Stores `productId` in environment.

3. **Create Order** (`/order/create-order`)
   - Places an order for the previously created product.
   - Stores `orderId` in environment.

4. **View Order Details** (`/order/get-orders-details`)
   - Fetches the order details using `orderId`.

5. **Delete Product** (`/product/delete-product/:productId`)
   - Deletes the created product to clean up data.

## 🧪 Test Scripts

Each request includes Postman test scripts to:
- Validate correct HTTP status codes (`200`, `201`)
- Assert expected response messages (e.g., "Login Successfully", "Product Added Successfully")
- Extract dynamic values (`token`, `productId`, `orderId`) and store them in environment variables for chained requests.

## ✅ Environment Variables

| Key         | Description                          |
|-------------|--------------------------------------|
| `base_Url`  | Base URL of the Ecommerce API        |
| `token`     | Bearer token retrieved after login   |
| `userId`    | ID of the logged-in user             |
| `productId` | ID of the created product            |
| `orderId`   | ID of the created order              |

## ▶️ How to Run

1. Open Postman.
2. Import both files:
   - Collection: `E2E Ecommerce API Test.postman_collection.json`
   - Environment: `E2E Ecommerce Env.postman_environment.json`
3. Select the imported environment from the top-right dropdown.
4. Run the collection using the Postman Runner to simulate the full e-commerce transaction.

## 🛠️ Author

**Moaz Sabry Mahmoud**  
Email: moazmosa71@gmail.com  
Phone: +201143434227
