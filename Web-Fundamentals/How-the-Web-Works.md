# How the Web Works

## Internet vs Web

The Internet and the Web are two different concepts.

### Internet

The Internet is the global network infrastructure that connects devices together. It allows computers and networks to communicate through hardware such as routers, cables, and wireless connections.

### Web

The Web (World Wide Web) is a service that runs on top of the Internet. It allows users to access information and resources through websites and web applications.

---

## Client and Server

### Client

A client is a device or application that sends requests to a server.

Examples:
- Web browsers (Chrome, Firefox)
- Mobile applications

The browser can act as a client by sending requests to web servers using URLs and protocols such as HTTP.

### Server

A server hosts resources and responds to client requests by delivering the requested resources.

Resources can include:
- HTML files
- Images
- Videos
- Links
- Other data

---

# DNS (Domain Name System)

DNS is a system that translates human-readable domain names into IP addresses.

Example:
google.com


Domain structure:

- `google` → Second-Level Domain (SLD)
- `.com` → Top-Level Domain (TLD)

Types of domains:

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

An IP address is a unique identifier assigned to devices connected to a network.

It allows devices to communicate with each other over the Internet.

---

# Types of Servers

## Web Server

Responsible for handling HTTP requests and returning web resources.

## Application Server

Responsible for running application logic and processing requests.

## Database Server

Responsible for storing and managing application data.

## Load Balancer

A load balancer distributes incoming requests between multiple servers to improve performance and availability.

---

# HTTP and HTTPS

## HTTP

HTTP stands for:

**HyperText Transfer Protocol**

It is a communication protocol used between clients and servers to exchange resources and data.

## HTTPS

HTTPS stands for:

**HyperText Transfer Protocol Secure**

It uses encryption through TLS to protect data transferred between the client and server.

---

# HTTP Methods

## GET

Used to retrieve data from a server.

Examples:
- Loading a webpage
- Downloading an image

## POST

Used to send data to a server.

Examples:
- Login forms
- Creating new resources

## PUT

Used to update existing resources.

## DELETE

Used to remove resources from a server.

---

# HTTP Status Codes

## 1xx - Informational

The request was received and the server is processing it.

## 2xx - Success

The request was successfully received and processed.

Example:
200 OK

## 3xx - Redirection

The client needs to take additional action.

Examples:
301 Moved Permanently
302 Found


## 4xx - Client Error

The request contains an error from the client side.

Examples:
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found


## 5xx - Server Error

The server failed while processing a valid request.

Example:
500 Internal Server Error


---

# HTTP/2

HTTP/2 improves web performance and efficiency through:

- Multiplexing
- Header compression
- Better resource handling

Security mainly depends on HTTPS/TLS.

---

# Cookies and Sessions

## Cookies

Cookies are small pieces of data stored by the browser and sent with HTTP requests.

They help websites remember users and maintain sessions.

Example:

1. The user logs in with a username and password.
2. The server verifies the credentials.
3. The server creates a session.
4. The browser stores a session ID in a cookie.
5. Future requests include the cookie to identify the user.

---

# Sessions

A session is a server-side mechanism used to maintain a user's state after authentication.

The server stores session information and connects it to a session ID.

---

# Tokens

A token is a temporary credential used to access protected resources.

Tokens can have:

- Expiration time
- Limited permissions
- Specific access rights

They allow users to access resources without sending their username and password with every request.

---

# Authentication and Authorization

## Authentication

Authentication is the process of verifying the identity of a user.

It answers:

**Who are you?**

Types of authentication:

### Something you know
Examples:
- Password
- PIN

### Something you have
Examples:
- Security key
- Phone

### Something you are
Examples:
- Fingerprint
- Biometrics

---

## Authorization

Authorization determines what resources or actions a user is allowed to access.

It answers:

**What are you allowed to do?**

---

# Same-Origin Policy (SOP)

Same-Origin Policy is a browser security mechanism that prevents a website from accessing sensitive data from another website with a different origin.

An origin is based on:

- Protocol
- Domain
- Port

---

# CORS

CORS stands for:

**Cross-Origin Resource Sharing**

It is a mechanism that allows servers to specify which external websites are allowed to access their resources.

Servers control this using HTTP headers such as:
Access-Control-Allow-Origin

