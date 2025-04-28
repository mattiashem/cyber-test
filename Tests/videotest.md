

# Video Test – Technical Questions Explanation

In this test, you are required to **record a video** where you explain answers to the following technical questions. The goal is to assess both your technical knowledge and your ability to clearly communicate complex concepts.

---

## 1. What Happens When You Enter "google.com" in a Browser and Press Enter?

**Question:**  
Describe the detailed technical steps that occur when a user enters a domain like `google.com` into the browser and presses Enter, until the webpage is fully loaded.

Key points to cover:

- The browser checks its local cache and the operating system's cache for a DNS record.
- If not cached, a **DNS query** is initiated to resolve the domain name into an IP address.
- Once the IP address is obtained, the browser opens a **TCP connection** to the server (typically on port 443 for HTTPS).
- A **TLS handshake** occurs to establish an encrypted connection, ensuring privacy and security.
- After the handshake, the browser sends an **HTTP(S) request** (e.g., a GET request) to the server.
- The server responds with the requested web content (HTML, CSS, JavaScript, images, etc.).
- The browser processes, parses, and renders the content to display the webpage to the user.

---

## 2. How Does DNS Work?

**Question:**  
Explain in detail how DNS (Domain Name System) works behind the scenes when resolving a domain name.

Key points to cover:

- When a device needs to resolve a domain like `google.com`, it queries its configured **upstream DNS server** (often provided by the ISP or a public resolver like Google DNS or Cloudflare DNS).
- If the upstream DNS server has the answer cached, it returns the IP address immediately.
- If not, the DNS server performs a **recursive lookup**:
  - It starts by querying a **root DNS server**.
  - The root server points to a **TLD (Top-Level Domain) server** (for `.com` domains).
  - The TLD server points to the **authoritative DNS server** responsible for the domain.
- The authoritative server provides the final IP address, and the result is sent back to the client.
- **Caching** at each level (client, resolver, server) speeds up future lookups until the **TTL (Time to Live)** value expires.

**Example Flow:**
1. Your device asks its DNS server: "What is the IP of google.com?"
2. If unknown, the server queries the root DNS server → the `.com` TLD server → Google's authoritative DNS server.
3. The authoritative server responds with the IP address.
4. The DNS server caches the result for faster future responses.
5. Your browser receives the IP address and connects to the server.

---

## 3. What Is the Difference Between a Document Database and an SQL (Relational) Database?

**Question:**  
Explain the major differences between a **document database** and an **SQL (relational) database**. Highlight differences in structure, flexibility, use cases, and examples.

**Comparison Table:**

| Aspect                  | SQL (Relational) Database                        | Document Database                             |
|--------------------------|--------------------------------------------------|------------------------------------------------|
| **Data Structure**       | Stores data in **tables** with rows and columns (strict structure). | Stores data in **documents** (JSON/BSON) with flexible, nested fields. |
| **Schema**               | **Fixed schema** — requires defined tables and columns; changes need migrations. | **Flexible schema** — documents can have varying structures. |
| **Query Language**       | Uses **SQL (Structured Query Language)** (e.g., `SELECT * FROM users WHERE age > 30`). | Uses **document queries**, often JSON-based (e.g., `find documents where age > 30`). |
| **Best For**             | Complex transactions, strong consistency, and structured data. | Rapid development, semi-structured or dynamic data, high scalability. |
| **Examples**             | MySQL, PostgreSQL, Microsoft SQL Server, Oracle. | MongoDB, Couchbase, Amazon DocumentDB, Firebase Firestore. |

**Summary:**  
- **SQL databases** are best when you need **strong consistency**, **relational data**, and **complex queries**.
- **Document databases** are ideal when you need **flexibility**, **speed**, and **scalability**, especially in applications with evolving data models.

---
Of course! Here's a question formatted like the ones above, focused on the difference between **TCP** and **UDP**:

---

## 4. What Is the Difference Between TCP and UDP Protocols?

**Question:**  
Explain the key differences between **TCP (Transmission Control Protocol)** and **UDP (User Datagram Protocol)**. Highlight how each protocol works, their use cases, and when one is preferred over the other.

**Comparison Table:**

| Aspect                  | TCP (Transmission Control Protocol)            | UDP (User Datagram Protocol)                 |
|--------------------------|-------------------------------------------------|-----------------------------------------------|
| **Connection**           | **Connection-oriented** — establishes a connection before data transfer (handshake). | **Connectionless** — sends data without setting up a connection. |
| **Reliability**          | Ensures reliable delivery: error checking, retransmission of lost packets. | No guarantee of delivery, order, or error correction. |
| **Speed**                | Slower due to overhead of connection and reliability features. | Faster due to minimal overhead. |
| **Ordering**             | Guarantees packet delivery **in order**. | No guarantee of packet order. |
| **Use Cases**            | Web browsing (HTTP/HTTPS), email (SMTP, IMAP), file transfers (FTP). | Streaming media (video/audio), VoIP, online gaming, DNS lookups. |
| **Examples of Protocols**| HTTP, HTTPS, FTP, SMTP.                        | DNS, DHCP, SNMP, video streaming. |

**Summary:**  
- **TCP** is ideal when **reliable and ordered delivery** is critical, even if it means slower performance.
- **UDP** is best when **speed and low latency** are more important than perfect reliability, such as in **real-time applications**.

---


# Final Notes for the Video:
- Speak clearly and explain **step-by-step**.
- Use examples whenever possible.
- Try to explain **as if teaching someone with basic technical knowledge** — clear and structured explanations are critical.

