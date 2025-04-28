

# DNS Knowledge Test – Networking Concepts

**Instructions:**  
You may use tools like `dig`, `nslookup`, `whois`, and online IP geolocation services. You are encouraged to perform tests using the Linux terminal or equivalent DNS lookup tools.

---

## 1. MX Record Location
**Question:**  
Look up the MX record for the domain `protonmail.com`.  
- What is the priority of the primary mail server?
- Use the IP address to determine the country where it is hosted.

**Expected Commands:**
```
dig protonmail.com MX
dig mail.protonmail.ch
```

**Correct Answer:** Switzerland

---

## 2. CNAME Chain Resolution
**Question:**  
- What is the CNAME of `www.wordpress.com`?
- What is the final IP address after resolution?

**Expected Commands:**
```
dig www.wordpress.com CNAME
dig [cname_result]
```

**Correct Answer:** wordpress.com

---

## 3. A Record and Provider
**Question:**  
- What is the A record IP address for `openai.com`?
- Does this IP belong to a cloud provider (e.g., AWS, GCP)?

**Expected Command:**
```
dig openai.com
```
Use services like `ipinfo.io` to determine IP ownership.

**Correct Answer:** Cloudflare, Inc.

---

## 4. TTL Interpretation
**Question:**  
- Determine the TTL (Time To Live) for `github.com`.
- What does the TTL value mean in terms of DNS caching?

**Expected Command:**
```
dig github.com
```

**Correct Answer:** 30 seconds / Time To Live (how long the DNS result is cached).

---

## 5. TXT Records
**Question:**  
- What are the TXT records for `google.com`?
- Which records relate to email authentication?

**Expected Command:**
```
dig google.com TXT
```

**Correct Answer:** `v=spf1`

---

## 6. Name Server Ownership
**Question:**  
- What are the NS records for `wikipedia.org`?
- Which organization provides these name servers?

**Expected Command:**
```
dig wikipedia.org NS
```
Check NS domain ownership using `WHOIS`.

**Correct Answer:** Donuts Inc.

---

## 7. Reverse DNS Lookup
**Question:**  
Perform a reverse DNS lookup on the IP address `8.8.8.8`.  
- What is the PTR (reverse DNS) record?

**Expected Command:**
```
dig -x 8.8.8.8
```

**Correct Answer:** dns.google

---

## 8. Zone Transfer Test
**Question:**  
Attempt a zone transfer from `zonetransfer.me` using its name server.  
- What type of record does the value `www.sydneyoperahouse.com` belong to?

**Expected Command:**
```
dig @nsztm1.digi.ninja zonetransfer.me AXFR
```

**Correct Answer:** staging.zonetransfer.me

---

## 9. WHOIS and DNS Match
**Question:**  
- Run a WHOIS lookup on `cloudflare.com`.
- Do the DNS NS records match the hosting provider found in the WHOIS information?

**Expected Commands:**
```
whois cloudflare.com
dig cloudflare.com NS
```

**Correct Answer:** No

---

## 10. CDN Detection
**Question:**  
- Check if `udemy.com` uses a Content Delivery Network (CDN).
- Use the DNS record chain to support your answer.

**Expected Command:**
```
dig www.udemy.com
```
Look for CDN patterns in CNAMEs (e.g., Akamai, Cloudflare, Fastly).

**Correct Answer:** Cloudflare

---

### Notes:
- Always validate your results with multiple tools where possible.
- Be aware that DNS records can change over time; answers may vary slightly depending on when the test is conducted.

