Here’s a clean, well-structured **GitHub revision note** you can directly copy into a README.md file.

---

# 🚀 NGINX, Apache & Web Servers – DevOps Revision Notes

## 📌 1. What is a Web Server?

A **web server** is software that:

* Listens for HTTP/HTTPS requests from browsers
* Sends back web content (HTML, CSS, JS, images)
* Or forwards requests to backend applications

### Example flow:

```text
Browser → Web Server → Response (Web Page)
```

### Popular web servers:

* Apache HTTP Server
* NGINX

---

## 📌 2. Apache HTTP Server (httpd)

Apache is a traditional web server used to:

* Serve static and dynamic web content
* Run PHP-based applications (WordPress, etc.)
* Handle requests using processes/threads

### Working:

```text
Browser → Apache → /var/www/html/index.html → Response
```

### Key points:

* Old and stable
* Easy to configure
* Uses process/thread-based architecture

---

## 📌 3. NGINX

NGINX is a high-performance web server used for:

* Serving static content
* Reverse proxy
* Load balancing
* HTTPS handling
* Caching and compression

### Working:

```text
Browser → NGINX → Response / Backend App
```

### Key points:

* Handles high traffic efficiently
* Event-driven architecture
* Lightweight and fast

---

## 📌 4. Web Server vs Reverse Proxy vs Load Balancer

### 🟢 Web Server

Serves files directly to users.

```text
Browser → NGINX/Apache → HTML file → Browser
```

---

### 🟡 Reverse Proxy

Forwards requests to backend applications.

```text
Browser → NGINX → App Server → Response
```

### Benefits:

* Hides backend servers
* Improves security
* Handles SSL (HTTPS)
* Central entry point

---

### 🔵 Load Balancer

Distributes traffic across multiple servers.

```text
Browser → NGINX
                ├→ App Server 1
                ├→ App Server 2
                └→ App Server 3
```

### Benefits:

* Prevents overload
* Improves availability
* Increases performance

---

## 📌 5. HTTP vs HTTPS

| Feature  | HTTP         | HTTPS                |
| -------- | ------------ | -------------------- |
| Security | ❌ Not secure | ✅ Secure (encrypted) |
| Port     | 80           | 443                  |
| Data     | Plain text   | Encrypted (SSL/TLS)  |

### Key idea:

HTTPS protects data using encryption.

---

## 📌 6. Why NGINX is used in front of applications?

Companies place NGINX before apps because:

* 🔐 Security (hides backend servers)
* ⚡ High performance
* 🔁 Load balancing
* 🔒 SSL/TLS termination
* 📁 Static file handling
* 🚀 Better scalability

---

## 📌 7. What happens when user opens a website?

```text
Browser
   ↓
NGINX / Apache
   ↓
Application Server
   ↓
Database
   ↓
Response back to Browser
```

---

## 📌 8. If a server crashes

NGINX:

* Stops sending traffic to failed server
* Redirects traffic to healthy servers
* Ensures high availability

---

## 📌 9. DevOps Key Concepts to Remember


Web Server → serves web pages
API → shares data between systems
App Server → runs backend logic
Reverse Proxy → forwards requests to backend
Load Balancer → distributes traffic
Database → stores data
---

## 📌 10. Simple One-Line Definitions

* **Apache** → Traditional web server
* **NGINX** → High-performance web server + reverse proxy + load balancer
* **Reverse Proxy** → Middleman between user and backend
* **Load Balancer** → Traffic distributor
* **HTTP** → Unencrypted web communication
* **HTTPS** → Encrypted web communication

---


📌 Web Server

A web server is software that receives requests from a browser and delivers web pages (HTML, CSS, images) or forwards requests to an application.

👉 Example: Apache, NGINX

📌 API (Application Programming Interface)

An API is a set of rules that allows applications to communicate and exchange data with each other, usually in JSON format.

📌 Application Server

An application server runs the backend logic of an application, processes data, and interacts with the database.

👉 Example: Node.js, Django, Spring Boot

📌 Reverse Proxy

A reverse proxy is a server that receives client requests and forwards them to backend servers, hiding the backend from users.

👉 Example: NGINX in front of apps

📌 Load Balancer

A load balancer distributes incoming traffic across multiple servers to improve performance and availability.

📌 Database

A database is a system used to store, manage, and retrieve structured data.

👉 Example: MySQL, PostgreSQL
