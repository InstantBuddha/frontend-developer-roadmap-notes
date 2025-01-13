# My notes on messwithdns.net

- [My notes on messwithdns.net](#my-notes-on-messwithdnsnet)
  - [URL](#url)
  - [DNS record types A and CNAME](#dns-record-types-a-and-cname)
  - [Other record types](#other-record-types)
  - [The TXT record type](#the-txt-record-type)
  - [Host Headers and Shared IP Addresses](#host-headers-and-shared-ip-addresses)
  - [Negative DNS caching](#negative-dns-caching)

## URL

[A fun page to learn about DNS](https://messwithdns.net/)

## DNS record types A and CNAME

In DNS (Domain Name System), **A** and **CNAME** records are two of the most common types, each serving a different purpose:

**A Record (Address Record)**
- **Purpose**: Maps a domain name to an IPv4 address.
- **Use Case**: When a user enters a domain like `example.com`, the DNS uses the A record to find the associated IP address (e.g., `192.0.2.1`). This lets their browser locate the server to connect to.
- **Example**:
  ```
  example.com.  IN  A  192.0.2.1
  ```
- **Key Point**: Each A record links a domain or subdomain to a single IP address. For IPv6 addresses, an "AAAA" record is used instead of an A record.

**CNAME Record (Canonical Name Record)**
- **Purpose**: Creates an alias for another domain name, allowing one domain to point to another.
- **Use Case**: Often used for subdomains or alternative names. For example, `www.example.com` can have a CNAME record pointing to `example.com`, meaning both will resolve to the same IP without needing separate A records.
- **Example**:
  ```
  www.example.com.  IN  CNAME  example.com.
  ```
- **Key Point**: A CNAME record does not directly link to an IP address but points to another domain name. That domain then resolves to an IP, creating an indirect link.

Using these records effectively can simplify DNS management, especially in cases where multiple domains or subdomains should resolve to the same IP.

## Other record types

Certainly! DNS records serve different purposes. Here's a brief overview of common types:

1. **MX (Mail Exchange) Record**  
   - Specifies the mail server responsible for receiving emails for a domain.
   - Example:  
     ```
     example.com.  IN  MX  10 mail.example.com.
     ```
   - The number (`10`) indicates priority; lower numbers have higher priority.

2. **TXT (Text) Record**  
   - Stores arbitrary text, often used for verification or configuration (e.g., SPF, DKIM, or DMARC for email security).
   - Example:  
     ```
     example.com.  IN  TXT  "v=spf1 include:_spf.google.com ~all"
     ```

3. **NS (Name Server) Record**  
   - Specifies the authoritative name servers for a domain.
   - Example:  
     ```
     example.com.  IN  NS  ns1.example.com.
     ```

4. **PTR (Pointer) Record**  
   - Used in reverse DNS lookups to map an IP address back to a hostname.
   - Example:  
     ```
     1.2.3.4.in-addr.arpa.  IN  PTR  example.com.
     ```

5. **SRV (Service) Record**  
   - Defines the location (hostname and port) of specific services like SIP or LDAP.
   - Example:  
     ```
     _sip._tcp.example.com.  IN  SRV  10 5 5060 sipserver.example.com.
     ```
   - Priority (`10`), weight (`5`), and port (`5060`) are included.

6. **AAAA Record**  
   - Maps a domain to an IPv6 address (similar to an A record for IPv4).
   - Example:  
     ```
     example.com.  IN  AAAA  2001:0db8:85a3:0000:0000:8a2e:0370:7334
     ```

7. **SOA (Start of Authority) Record**  
   - Contains administrative information about the zone, including the primary name server, email of the admin, and settings like refresh and retry intervals.
   - Example:  
     ```
     example.com.  IN  SOA  ns1.example.com. admin.example.com. 2023111501 7200 3600 1209600 3600
     ```

8. **CAA (Certification Authority Authorization) Record**  
   - Specifies which certificate authorities are allowed to issue SSL/TLS certificates for the domain.
   - Example:  
     ```
     example.com.  IN  CAA  0 issue "letsencrypt.org"
     ```

9. **TTL (Time-to-Live)**  
   - Not a record type but an attribute specifying how long a DNS record should be cached by resolvers.

Each record type serves a distinct purpose, and understanding them helps in managing and troubleshooting DNS configurations. Let me know if you'd like more details on any specific type!

## The TXT record type

A **TXT (Text) Record** in DNS allows domain administrators to store text-based information that other systems can retrieve. Although its name suggests general text storage, it is widely used for various configuration and verification purposes in modern DNS setups.

**Common Uses of TXT Records:**
1. **SPF (Sender Policy Framework)**  
   Helps prevent email spoofing by specifying which mail servers are authorized to send emails for the domain.  
   Example:  
   ```
   example.com. IN TXT "v=spf1 include:_spf.google.com ~all"
   ```

2. **DKIM (DomainKeys Identified Mail)**  
   Stores the public key for email authentication to verify that the email has not been altered.  
   Example:  
   ```
   default._domainkey.example.com. IN TXT "v=DKIM1; k=rsa; p=MIIBIjANBgkqh...long_key"
   ```

3. **DMARC (Domain-based Message Authentication, Reporting, and Conformance)**  
   Provides instructions on how to handle emails failing SPF or DKIM checks and collects reports about email delivery.  
   Example:  
   ```
   _dmarc.example.com. IN TXT "v=DMARC1; p=reject; rua=mailto:dmarc-reports@example.com"
   ```

4. **Domain Verification**  
   Used to verify domain ownership for services like Google, Microsoft, or SSL certificate providers.  
   Example:  
   ```
   example.com. IN TXT "google-site-verification=abcdef123456"
   ```

5. **General Information**  
   TXT records can store any descriptive text or metadata for a domain.  
   Example:  
   ```
   example.com. IN TXT "This is a text record for example.com."
   ```

**Format of a TXT Record:**
- **Name**: The domain or subdomain (e.g., `example.com`, `default._domainkey.example.com`).
- **TTL**: Time-to-live for caching the record.
- **Type**: TXT.
- **Value**: The text string (can include structured data like SPF or DKIM settings).

TXT records are highly versatile and widely used in DNS for managing email security, domain verification, and more!

## Host Headers and Shared IP Addresses

[See my notes in an other repo of mine with a working example of a Dockerized Nginx](https://github.com/InstantBuddha/nginx-notes/blob/main/Host-headers-and-shared-ip-addresses.md)

## Negative DNS caching

Negative caching in DNS refers to the practice of caching the fact that a DNS record does not exist. When a DNS resolver queries for a domain name or record and receives a response indicating that it doesn’t exist (e.g., an NXDOMAIN response), the resolver temporarily stores this information. 

This caching prevents repeated queries for the same non-existent record, reducing unnecessary load on DNS servers and speeding up subsequent queries. The duration for which the absence is cached is determined by the **SOA (Start of Authority) record**'s `negative TTL` (Time-to-Live) value.

