

# Web and Service Test

This test evaluates your ability to investigate a web service using standard network tools.  
**All tasks must be performed against the domain: urvalsprov.se

---

## 1. Web Server Fingerprint
**Question:**  
- What is the name of the web server being used?

**Expected Command:**
```
curl -v urvalsprov.se
```

**Correct Answer:** Apache

---

## 2. TLS Versions
**Question:**  
- Is TLS 1.0 versions on the web server configured ?

**Correct Answer:** Yess

---

## 3. TLS Certificate Signer
**Question:**  
- Who is the trusted signer Issuer CN of the TLS certificate?

**Correct Answer:** R10

---

## 4. What OS is the server running ?
**Question:**  
- What is the Os of the server 

**Note:** 


**Correct Answer:** Debian ore Ubuntu 
---

## 5. Database in Use
**Question:**  
- If WordPress is not using a MySQL database, which database system is being used instead?

**Correct Answer:** MariaDB

---

## 6. Open Ports
**Question:**  
- Besides ports 80, 22, 443, and 9200, are there any other open ports on the server?  
  - If yes, specify which port.

**Correct Answer:** 8081

---

## 7. Server Hosting Location
**Question:**  
- Where is the server physically hosted, and which company is hosting it?

**Correct Answer:** Finland

---

## 8. SSH Password Authentication
**Question:**  
- Is it possible to log in to the SSH server using a username and password?

**Correct Answer:** Yes

---

## 9. SSH Key Exchange Algorithms
**Question:**  
- Does the SSH server support the following key exchange algotithms diffie-hellman-group14-sha256 ?

**Note:** 

**Correct Answer:** Yes


---

## 10. Service on Port 9200
**Question:**  
- What service is running on port 9200?

**Correct Answer:** Elasticsearch

---

### Additional Notes:
- Always validate your results with real network testing tools (`curl`, `nmap`, `openssl`, `ssh`, etc.).
- Some services may be behind firewalls or may restrict probing; act responsibly and legally.
- Answers might vary depending on when the test is performed due to server updates or configuration changes.

