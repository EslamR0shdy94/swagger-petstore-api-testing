# 🐾 Swagger Petstore - Manual API Testing Project

## 📌 Project Overview

This project focuses on **manual API testing** for the [Swagger Petstore](https://petstore.swagger.io) API using **Postman**.  
It covers full **CRUD operations** for pets, along with **auth tests**, and includes both **positive and negative** test scenarios.

The goal is to validate the main functionalities of the API, understand request–response structures, and practice writing assertions using Postman tests.

---

## 🔗 API Information

- **Base URL:** `https://petstore.swagger.io/v2`
    
- **Authentication:** API Key (`api_key`) header supported.
    
- OperationMethodEndpointCreate PetPOST`/pet`Get Pet by IDGET`/pet/{petId}`Update PetPUT`/pet`Delete PetDELETE`/pet/{petId}`User InfoGET`/user/{username}`
    

---

## 🧪 Tools Used

- **Postman** → for API testing and assertions
    
- **Swagger Docs** → for exploring endpoints
    
- **JSON Formatter** → for pretty-printing API responses
    
- **Newman (optional)** → for running the Postman collection via CLI and generating reports
    

---

## 🧩 Test Coverage

### ✅ Functional Tests

- Verify CRUD operations on `/pet` endpoint.
    
- Verify user details retrieval via `/user/{username}`.
    
- Validate correct response codes (200, 404, etc.).
    

### ⚠️ Negative Tests

- Create pet with missing fields → expect 400 or error message.
    
- Get pet by invalid ID → expect 404 Not Found.
    
- Delete pet twice → second delete should fail gracefully.
    

### 🔁 Regression Tests

- Re-run main functional tests to confirm stable functionality after updates.
    
- Validate that all endpoints return consistent schema and structure.
    

---

## ⚙️ Environment Setup

### 🔸Environment Variables

| **Variable** | **Value** | **Description** |
| --- | --- | --- |
| `base_url` | `https://petstore.swagger.io/v2` | Base URL of Swagger Petstore API |
| `user_name` | `eslam22` | Username used for login and user creation tests |
| `user_password` | `83r5^._` | Password for test user |
| `token` | _(dynamic)_ | Authentication token (if returned from login) |
| `user_email` | `eslam@example.com` | Default email used in user creation |
| `usersList` | `["roshdyjr","marwan5"]` | Static list of usernames for batch creation |
| `usersArray` | `["ahmed_f","mona_s"]` | Additional test user array |
| `order_id` | _(dynamic)_ | Used to store order ID after placing an order |
| `rex_id` | `3` | Pet ID for Rex (test pet) |
| `cat_id` | `4` | Pet ID for Cat (test pet) |
| `api_key` | `special-key` | API key used for authenticated endpoints |
| `delete_pet_id` | `158` | Pet ID reserved for delete tests |

## 🚀 How to Run Tests

### 🧭 In Postman:

1. Import the collection:  
    `Collections/SwaggerPetstore.postman_collection.json`
    
2. Import the environment:  
    `Environments/Petstore.postman_environment.json`
    
3. Set the `base_url` and `api_key` values.
    
4. Run individual requests manually **or** execute the entire collection using **Collection Runner**.
    
5. Check results and take screenshots of test reports.
    

## 📂 Project Structure
```bash

Swagger-Petstore-API-Testing/  
│  
├── 📁 Collections/  
│ └── SwaggerPetstore.postman_collection.json  
│  
├── 📁 Environments/  
│ └── Petstore.postman_environment.json  
│  
├── 📁 Screenshots/  
│ └── example_test_results.png  
│  
└── README.md
```
---
✅ Results  
All endpoints were tested successfully:

Status codes validated (200, 201, 400, 404)

Request chaining with variables tested successfully

All CRUD operations completed for Users, Products, and Carts

## 🧪 Test Coverage
- ✅ Pets CRUD operations  
- ✅ Find pets by status  
- ✅ Users CRUD and login/logout  
- ✅ Store orders and inventory  

---

## 🧠 Author
**Eslam Roshdy**  
📧 esroshdy22@gmail.com  
🔗 [GitHub Profile](https://github.com/EslamR0shdy94)
