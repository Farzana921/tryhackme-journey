**DNS Learning Summary**

🔗 Room Link: [Red Team Engagements](https://tryhackme.com/room/dnsindetail)

### 1. What is DNS?

* **DNS (Domain Name System)** translates human-readable domain names (like `tryhackme.com`) into IP addresses (like `104.26.10.229`).
* Every device on the internet has a unique IP address.
* DNS allows me to use simple names instead of memorizing numeric addresses.

**What I Learned:**

* The purpose of DNS.
* The difference between domain names and IP addresses.
* How DNS makes internet navigation easier.



### 2. Domain Hierarchy

* **TLD (Top-Level Domain):** Rightmost part of a domain, e.g., `.com`. Types include:

  * **gTLD:** Generic (e.g., `.com`, `.org`, `.edu`)
  * **ccTLD:** Country Code (e.g., `.co.uk`, `.ca`)
* **Second-Level Domain:** The name registered under the TLD, e.g., `tryhackme` in `tryhackme.com`.
* **Subdomain:** Comes before the Second-Level Domain, e.g., `admin` in `admin.tryhackme.com`.

**Rules and Limits:**

* Max length of a subdomain: **63 characters**
* Max length of a full domain: **253 characters**
* Invalid subdomain character: **underscore (\_)**
* `.co.uk` is a **ccTLD**

**What I Learned:**

* Structure of domain names.
* Character rules and length limits.
* The difference between TLDs, Second-Level Domains, and Subdomains.


### 3. DNS Record Types

* **A Record:** Maps to an IPv4 address (e.g., `104.26.10.229`).
* **AAAA Record:** Maps to an IPv6 address (e.g., `2606:4700:20::681a:be5`).
* **CNAME Record:** Maps one domain to another (e.g., `store.tryhackme.com` → `shops.shopify.com`).
* **MX Record:** Defines mail servers for a domain with priority flags.
* **TXT Record:** Stores text-based data (used for email validation, domain verification, etc.).

**What I Learned:**

* Different DNS record types and their uses.
* How DNS supports services beyond just websites (e.g., email).
* The distinction between IPv4 (A) and IPv6 (AAAA).



### 4. Making a DNS Request

* **Step 1:** My computer checks **local cache**.
* **Step 2:** Queries a **Recursive DNS Server** (often provided by ISP).
* **Step 3:** If not cached, the request goes to a **Root DNS Server**.
* **Step 4:** Root server points to the relevant **TLD server**.
* **Step 5:** TLD server refers to the **Authoritative DNS Server**.
* **Step 6:** Authoritative server provides the DNS record.

**Important Terms:**

* **Recursive DNS Server:** Provided by ISP, handles the lookup process.
* **Root Server:** Points to TLD servers.
* **TLD Server:** Directs to authoritative servers.
* **Authoritative Server:** Stores the actual DNS records.
* **TTL (Time To Live):** Duration (in seconds) that a DNS record is cached.

**What I Learned:**

* The step-by-step flow of a DNS request.
* The purpose of DNS caching and how it improves performance.
* The role of each type of DNS server.



### 5. Practical (DNS Query Examples)

Using DNS tools, I discovered:

* **CNAME of `shop.website.thm`:** `shops.myshopify.com`
* **TXT record of `website.thm`:** `THM{7012BBA60997F35A9516C2E16D2944FF}`
* **MX record priority:** `30`
* **A record of `www.website.thm`:** `10.10.10.10`

**What I Learned:**

* How to perform real DNS lookups.
* How to interpret the output from DNS records.
* Hands-on understanding of A, MX, CNAME, and TXT records.



**Overall Takeaway:**
I’ve learned how DNS works, the types of records it uses, how domains are structured, and how DNS queries are processed in practice. This knowledge forms a solid foundation for understanding internet communication and managing domains.
