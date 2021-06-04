# Cheatsheet 💻 - DNS, HTTP, TLS - HTTPS 

###### Troubleshooting HTTP Requests

When accessing a web server or application, every HTTP request that is received by a server is responded to with an HTTP status code. HTTP status codes are three-digit codes all groupd in five type of classes:

```
1xx: Informational
2xx: Success
3xx: Redirection
4xx: Client Error
5xx: Server Error
```
----------------------------------------------------------------------------------------------------------------------------

## DNS

Video Deep Dive DNS: https://www.youtube.com/watch?v=DV0q9s94RL8

###### DNS: Is a protocol and it's shrot for Domain Name System (DNS) to make it simple, is the phonebook of the Internet Protocol. 

In further detail DNS will translate domain names to IP addresses so any browser can load the website you would like to visit.

In a nutshell 🥜 DNS will convert a hostname / domain like www.google.com into a computer-friendly IP Addresss.

## Four DNS Servers are involved in the process: 
Here is a quick recap of this process

**DNS Recursor:**
Is the first stop in a DNS query 🛑
The recursive resolver acts as a middleman between a client (you) and a DNS nameserver. After receiving a DNS query from a web client (the browser you are using), a recursive resolver will either respond with cached data, or send a request to a root nameserver, followed by another request to a TLD nameserver, and then one last request to an authoritative nameserver.Once all the request are completed you will be able to see the webite your are looking to visit.


**Root Server:** 
The Root Server is in charge of resolving that human-readable hostname into a computer-friendly IP address. 
This server manages the root zone, this server it's at the top of the hierchachy. During the event of an uncached DNS query, whenever a user enters a web address into their browser, this action triggers a DNS lookup, and all DNS lookups start at the root zone. 


**TLD - Top Level Domain:** 
This server is more specific in the tasks that it has to manage. A TLD nameserver maintains / manages all information for the domain names that share a common domain extension, for example as .com, .net, .gov  or whatever comes after the last dot in a url. 


**Authoritave Nameserver:**
This is the resolver's last step. 
The authoritative nameserver contains information specific to the domain name it serves and it can provide a recursive resolver with the IP address of that server found in the DNS A record, or if the domain has a CNAME record (alias). it will provide the recursive resolver with an alias domain, at which point the recursive resolver will have to perform a whole new DNS lookup to procure a record from an authoritative nameserver (often an A record containing an IP address).

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
###### My go to commands / tools  when troubleshooting DNS are listed below with quick explanation below:

**nslookup -** 

![nslookup](https://github.com/mespada829/cheatsheet/blob/Images/nslookup.png)

From this, we can see the IP address and the DNS server that serve it. 

**Dig -** 

![dig](https://github.com/mespada829/Cheatsheet-DNS-TLS-Etc/blob/master/dig.png)

Dig displays a QUESTION SECTION (the request) and an ANSWER SECTION (what the DNS server sends in response to the request).


**Ping -**

![ping](https://github.com/mespada829/Cheatsheet-DNS-TLS-Etc/blob/master/ping.png)

If the remote host is active and configured to respond to ping requests, responses appear. 

**Free DNS Site Tool -** For example, to test if DNS propagation is complete, you can visit http://www.whatsmydns.net and specify a domain name. The site displays a global map showing the IP address associated with the domain name for a variety of DNS servers around the world.
