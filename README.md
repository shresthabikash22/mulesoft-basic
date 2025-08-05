# Customer Info API (MuleSoft)

## Description
Simple Mulesoft project 
The **Customer Info API** provides a set of endpoints to manage customer data and retrieve associated order information. Built using **MuleSoft**, this API follows RESTful principles and supports the full range of **CRUD operations**:

- **Create** new customers
- **Read** customer details and their orders
- **Update** existing customer records
- **Delete** customers from the system

This API is designed for integration with frontend applications and core systems, enabling seamless customer data management.

---
## BaseURL
  http://localhost:8081

## 🔹Endpoints
### 🔍 `GET /customer?customerId=1`
- **Description**: Retrieves customer info along with their orders.
- **Query Parameter**: `customerId` (required)
  | Name         | Type   | Required | Description                         |
  |--------------|--------|----------|------------------------------------ |
  | customerId   | int    | ✅ Yes   | Unique identifier of the customer  |
- **Sample Request**:
  
---
- **Response**: JSON with customer and orders(default data for now).
  ```json
{
  "customerId": 123,
  "name": "John Doe",
  "email": "john@example.com",
  "orders": [
    {
      "orderId": 1,
      "product": "Laptop",
      "amount": 1000
    },
    ...
  ]
}  ```
---
### Future Enhancement
### ➕ `POST /customer`
- **Description**: Creates a new customer record.
- **Payload**: JSON with customer fields.
- **Response**: Confirmation with generated `customerId`.
---

### ♻️ `PUT /customer`
- **Description**: Updates customer data.
- **Payload**: Full JSON object of customer with existing `customerId`.
- **Response**: Success/failure message.

---

### ❌ `DELETE /customer?customerId=1`
- **Description**: Deletes the specified customer.
- **Query Parameter**: `customerId` (required)
- **Response**: Deletion status message.
