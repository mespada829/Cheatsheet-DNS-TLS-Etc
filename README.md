# Cheatsheet 💻

**DNS** - The Domain Name System (DNS) to make it simple, is the phonebook of the Internet. 
In further detail DNS will translate domain names to IP addresses so any browser can load the website you would like to visit.

In a nutshell DNS will convert a hostname / domain like www.google.com into a computer-friendly IP Addresss.

## Four DNS Servers are involved in the process of loading a website:


###### DNS Resource Records:

**Name:** Is an alphanumeric identifier of the DNS record

**TTL (time to live):** Specifies how long the record should be kept in local cache

**Record Class** Indicates the namespace—typically IN, the Internet namespace

**Record Type:** Is the DNS record type—for example an A, CNAME, MX

**Record Data** Contains the DNS values, for example the IP address for a hostname

----------------------------------------------------------------------------------------------------------------------------

**The most common DNS record types supported by the DNS protocol:**

**Name Server records (NS):** Specifies the authoritative name server for a DNS zone

**IPv4 Address Mapping records (A):** A hostname and its IPv4 address

**IPv6 Address records (AAAA):** A hostname and its IPv6 address

**Canonical Name records (CNAME):** Points a hostname to an alias

**Mail eXchanger record (MX):** Specifies an SMTP email server for the domain
