# Frontend, Backend and API

Understanding the difference between Frontend, Backend, and APIs is essential for understanding how modern web applications work.

---

# Frontend

Frontend is the part of a web application that users can see and interact with directly.

It is responsible for creating the user interface (UI) and handling user interactions.

Examples:

- Web pages
- Buttons
- Forms
- Images
- Layout and design
- User interface (UI)

Frontend runs mainly inside the user's browser and is built using technologies such as:

- HTML
- CSS
- JavaScript

Example:

A login page where the user enters a username and password is part of the frontend.

---

# Backend

Backend is the part of a web application that works behind the scenes.

It is responsible for processing requests, applying application logic, managing data, and communicating with databases.

Backend responsibilities:

- Processing user requests
- Application logic
- Database communication
- User authentication
- User authorization
- Data processing

Examples of backend data:

- User accounts
- Search history
- Orders
- Messages
- User permissions

Backend applications run on servers using programming languages such as:

- JavaScript (Node.js)
- Python
- Java
- PHP
- C#

Example:

When a user logs in, the backend:

1. Receives the login request.
2. Checks the credentials.
3. Queries the database.
4. Creates a session or token.
5. Returns a response to the frontend.

---

# API (Application Programming Interface)

API stands for:

**Application Programming Interface**

An API is a set of rules and endpoints that allows different software components to communicate and exchange data.

In web applications, APIs allow the frontend to communicate with backend services.

An API is usually part of the backend and exposes endpoints that clients can interact with.

---

# How Frontend, API, Backend and Database Work Together

Example: User Login

1. The user enters credentials in the frontend.
2. The frontend sends an HTTP request to an API endpoint.
3. The API receives the request and passes it to the backend logic.
4. The backend checks the database.
5. The backend creates a response.
6. The API sends the response back to the frontend.

Communication flow:

```
Frontend
    |
    | HTTP Request
    ↓
API Endpoint
    |
    ↓
Backend Logic
    |
    ↓
Database

Database
    |
    ↓
Backend Logic
    |
    ↓
API Response
    |
    ↓
Frontend
```

---

# API Data Formats

APIs commonly exchange data using:

## JSON

Example:

```json
{
  "username": "wiener",
  "password": "peter"
}
```

Response example:

```json
{
  "token": "example_token",
  "status": "success"
}
```

---

## XML

Example:

```xml
<user>
    <username>wiener</username>
</user>
```

---

# Common API Protocols

## REST API

REST (Representational State Transfer) is the most common type of web API.

It uses HTTP methods:

- GET
- POST
- PUT
- PATCH
- DELETE

Example:

```
GET /api/users/1
```

---

## GraphQL

GraphQL allows clients to request specific data from an API.

Example:

```graphql
{
  user {
    username
    email
  }
}
```

---

## SOAP

SOAP is an XML-based protocol used mainly in enterprise applications.

---

# API Security

APIs are an important target in web security because they handle sensitive data and functionality.

Common API vulnerabilities:

- Broken Access Control
- Authentication flaws
- Information Disclosure
- SQL Injection
- Path Traversal
- Server-Side Request Forgery (SSRF)

Security testing focuses on checking whether:

- Users can access unauthorized resources.
- Authentication is properly implemented.
- Sensitive data is protected.
- Input validation is correctly applied.

---

# Key Takeaways

- Frontend is the user-facing part of a web application.
- Backend handles application logic and data processing.
- APIs allow communication between frontend and backend.
- APIs commonly use HTTP and exchange data using JSON or XML.
- Security decisions must always be enforced on the backend.
- Understanding APIs is essential for web security testing.
