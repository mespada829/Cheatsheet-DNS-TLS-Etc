# Cheatsheet 💻 - DNS, HTTP, TLS - HTTPS 

###### DNS: The Domain Name System (DNS) to make it simple, is the phonebook of the Internet Protocol. 
In further detail DNS will translate domain names to IP addresses so any browser can load the website you would like to visit.

In a nutshell 🥜 DNS will convert a hostname / domain like www.google.com into a computer-friendly IP Addresss.

## Four DNS Servers that are involved in the process: 

**DNS Recursor:**
Is the first stop in a DNS query 🛑
The recursive resolver acts as a middleman between a client (you) and a DNS nameserver. After receiving a DNS query from a web client (the browser you are using), a recursive resolver will either respond with cached data, or send a request to a root nameserver, followed by another request to a TLD nameserver, and then one last request to an authoritative nameserver.Once all the request are completed you will be able to see the webite your are looking to visit.

**Root Server:** 
The Root Server is in charge of resolving that human-readable hostname into a computer-friendly IP address. 


**TLD - Top Level Domain:**

**Authoritave Nameserver:**

----------------------------------------------------------------------------------------------------------------------------

## DNS Resource Records:

**Name:** Is an alphanumeric identifier of the DNS record

**TTL (time to live):** Specifies how long the record should be kept in local cache

**Record Class** Indicates the namespace—typically IN, the Internet namespace

**Record Type:** Is the DNS record type—for example an A, CNAME, MX

**Record Data** Contains the DNS values, for example the IP address for a hostname


**The most common DNS record types supported by the DNS protocol:**

**Name Server records (NS):** Specifies the authoritative name server for a DNS zone

**IPv4 Address Mapping records (A):** A hostname and its IPv4 address

**IPv6 Address records (AAAA):** A hostname and its IPv6 address

**Canonical Name records (CNAME):** Points a hostname to an alias

**Mail eXchanger record (MX):** Specifies an SMTP email server for the domain

----------------------------------------------------------------------------------------------------------------------------

## How to troubleshoot DNS 

