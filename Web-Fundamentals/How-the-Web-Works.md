# 🌐 How the Web Works

## Internet vs Web

The Internet and the Web are two different concepts.

### Internet

The Internet is the global network infrastructure that connects devices together. It allows computers and networks to communicate through routers, cables, and wireless connections.

### Web

The Web (World Wide Web) is a service that runs on top of the Internet. It allows users to access websites and web applications through web browsers.

---

# URL Structure

Example:

```
https://example.com:443/products?id=10#reviews
```

| Component | Description |
|------------|-------------|
| `https` | Protocol |
| `example.com` | Domain |
| `443` | Port |
| `/products` | Path |
| `?id=10` | Query Parameter |
| `#reviews` | Fragment (Processed by the browser and not sent to the server) |

---

# Client and Server

## Client

A client is a device or application that sends requests to a server.

Examples:

- Web browsers
- Mobile applications
- Desktop applications

The browser acts as a client by sending HTTP requests to web servers.

## Server

A server receives client requests, processes them, and returns the requested resources.

Resources may include:

- HTML pages
- Images
- Videos
- JSON data
- Files
- APIs

---

# DNS (Domain Name System)

DNS translates human-readable domain names into IP addresses.

Example:

```
google.com
        ↓
142.250.xxx.xxx
```

## Domain Structure

```
google.com
```

- `google` → Second-Level Domain (SLD)
- `.com` → Top-Level Domain (TLD)

### gTLD (Generic Top-Level Domain)

Examples:

- `.com`
- `.org`
- `.net`

### ccTLD (Country Code Top-Level Domain)

Examples:

- `.ma`
- `.uk`
- `.fr`

---

# IP Address

An IP address is a unique identifier assigned to a device connected to a network.

It enables communication between devices over the Internet.

---

# Types of Servers

## Web Server

Handles HTTP requests and serves web resources.

Examples:

- Apache
- Nginx
- IIS

---

## Application Server

Processes application logic and generates responses.

Examples:

- PHP
- Node.js
- Java
- Python

---

## Database Server

Stores and manages application data.

Examples:

- MySQL
- PostgreSQL
- Microsoft SQL Server
- MongoDB

---

## Load Balancer

Distributes incoming traffic across multiple servers to improve availability and performance.

---

# HTTP and HTTPS

## HTTP

**HyperText Transfer Protocol**

A communication protocol used between clients and servers.

---

## HTTPS

**HyperText Transfer Protocol Secure**

HTTPS encrypts communication using TLS to protect transmitted data.

---

# HTTP Request

Example:

```http
GET /account?id=1 HTTP/1.1
Host: example.com
Cookie: session=abc123
User-Agent: Mozilla/5.0
```

### Components

- Request Line
- Headers
- Body (Optional)

---

# HTTP Response

Example:

```http
HTTP/1.1 200 OK
Content-Type: text/html
Set-Cookie: session=abc123

<html>...</html>
```

### Components

- Status Line
- Headers
- Body

---

# HTTP Methods

## GET

Retrieves data from the server.

Examples:

- Opening a webpage
- Viewing a profile
- Downloading an image

---

## POST

Sends data to the server.

Examples:

- Login
- Registration
- Creating resources

---

## PUT

Updates an existing resource.

---

## DELETE

Deletes a resource.

---

# HTTP Status Codes

## 1xx — Informational

The request has been received.

---

## 2xx — Success

Examples:

- 200 OK
- 201 Created
- 204 No Content

---

## 3xx — Redirection

Examples:

- 301 Moved Permanently
- 302 Found

---

## 4xx — Client Errors

Examples:

- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found

---

## 5xx — Server Errors

Examples:

- 500 Internal Server Error
- 502 Bad Gateway
- 503 Service Unavailable

---

# Common HTTP Headers

## Request Headers

- Host
- Cookie
- Authorization
- User-Agent
- Referer
- Origin
- Accept
- Content-Type

---

## Response Headers

- Set-Cookie
- Location
- Server
- Content-Type
- Content-Length
- Access-Control-Allow-Origin

---

# Content Types (MIME Types)

Examples:

```
text/html
application/json
application/xml
text/css
application/javascript
image/png
image/jpeg
```

---

# HTTP/2

HTTP/2 improves web performance through:

- Multiplexing
- Header Compression
- Faster Resource Loading

Security still depends on HTTPS (TLS).

---

# URL Encoding

Examples:

| Character | Encoded |
|-----------|----------|
| Space | `%20` |
| `/` | `%2F` |
| `.` | `%2E` |

Example:

```
../../../etc/passwd
```

URL Encoded:

```
..%2F..%2F..%2Fetc%2Fpasswd
```

Double URL Encoded:

```
..%252F..%252F..%252Fetc%252Fpasswd
```

---

# Cookies and Sessions

## Cookies

Cookies are small pieces of data stored in the browser and sent with every request.

Example:

1. User logs in.
2. Server verifies credentials.
3. Server creates a session.
4. Browser stores the session ID inside a cookie.
5. Future requests include the cookie.

---

## Cookie Attributes

- Secure
- HttpOnly
- SameSite
- Expires
- Max-Age

---

## Sessions

A session is server-side storage that keeps track of authenticated users.

The browser stores only the Session ID.

---

# Tokens

A token is a temporary credential used to access protected resources.

Common properties:

- Expiration Time
- Limited Permissions
- Access Scope

Example:

```
JWT
OAuth Access Token
API Token
```

---

# Authentication and Authorization

## Authentication

Authentication verifies a user's identity.

**Question:**

> Who are you?

Examples:

### Something You Know

- Password
- PIN

### Something You Have

- Phone
- Security Key

### Something You Are

- Fingerprint
- Face Recognition

---

## Authorization

Authorization determines what an authenticated user is allowed to access.

**Question:**

> What are you allowed to do?

---

# User-Controlled Input

User-controlled input is any data that can be modified by the user before reaching the server.

Examples:

```
?id=1

role=user

filename=image.jpg

Cookie

Headers

JSON Body
```

**Golden Rule**

> Never trust user-controlled input.

---

# Client Side vs Server Side

## Client Side

Runs inside the browser.

Examples:

- HTML
- CSS
- JavaScript

---

## Server Side

Runs on the server.

Examples:

- PHP
- Java
- Python
- Node.js
- C#
- Go

**Important**

Security decisions must always be enforced on the server side.

---

# Same-Origin Policy (SOP)

Same-Origin Policy is a browser security mechanism that prevents websites from reading data from another origin.

An origin consists of:

- Protocol
- Domain
- Port

Example:

```
https://example.com
```

cannot access

```
https://another.com
```

because the origins are different.

---

# CORS (Cross-Origin Resource Sharing)

CORS allows servers to specify which origins are allowed to access their resources.

Example:

Request:

```http
Origin: https://example.com
```

Response:

```http
Access-Control-Allow-Origin: https://example.com
```

---

# Key Takeaways

- The Internet is the network, while the Web is a service running on top of it.
- Clients send requests, and servers process and respond to them.
- DNS translates domain names into IP addresses.
- HTTP is used for communication, while HTTPS secures it using TLS.
- Sessions and cookies maintain user authentication.
- Authentication verifies identity, while authorization determines permissions.
- Never trust user-controlled input.
- Security decisions must always be enforced on the server side.
- SOP protects users by restricting cross-origin access, while CORS allows controlled exceptions.
