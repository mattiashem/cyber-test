

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
- What TLS versions is the web server configured to support?

**Correct Answer:** TLS 1.3

---

## 3. TLS Certificate Signer
**Question:**  
- Who is the trusted signer (Certificate Authority) of the TLS certificate?

**Correct Answer:** Let's Encrypt

---

## 4. WordPress Version
**Question:**  
- What is the version of WordPress being used on the site?

**Note:** No answer is currently provided; you should identify the version by investigating metadata or page source if available.

---

## 5. Database in Use
**Question:**  
- If WordPress is not using a MySQL database, which database system is being used instead?

**Correct Answer:** MariaDB

---

## 6. Open Ports
**Question:**  
- Besides ports 80, 22, 443, and 555, are there any other open ports on the server?  
  - If yes, specify which port.

**Correct Answer:** 10001

---

## 7. Server Hosting Location
**Question:**  
- Where is the server physically hosted, and which company is hosting it?

**Correct Answer:** Germany

---

## 8. SSH Password Authentication
**Question:**  
- Is it possible to log in to the SSH server using a username and password?

**Correct Answer:** No

---

## 9. SSH TLS Version
**Question:**  
- What TLS (or SSH) protocol version is the OpenSSH server configured to support?

**Note:** No answer is currently provided; use tools like `ssh -vvv` or `nmap` to determine.

---

## 10. Service on Port 555
**Question:**  
- What service is running on port 555?

**Correct Answer:** Elasticsearch

---

### Additional Notes:
- Always validate your results with real network testing tools (`curl`, `nmap`, `openssl`, `ssh`, etc.).
- Some services may be behind firewalls or may restrict probing; act responsibly and legally.
- Answers might vary depending on when the test is performed due to server updates or configuration changes.

