# Domain Name System (DNS)
DNS is a system that translates human-readable domain names into IP addresses so computers can communicate over the internet. It works in a hierarchical and distributed manner to efficiently resolve queries. DNS ensures users can access websites without remembering numeric IP addresses. It also improves performance using caching.

- Provides name-to-address resolution
- Uses a hierarchy (Root, TLD, Authoritative servers)
- Improves speed using caching mechanisms

### Example: 

When you enter google.com in a browser, DNS converts it into an IP address (like 142.x.x.x), allowing your system to connect to the correct server.

## Working

The DNS process can be broken down into several steps, ensuring that users can access websites by simply typing a domain name into their browser.
- User Input: The user enters a domain name (e.g., www.geeksforgeeks.org) in the browser.
- Local Cache Check: The browser or OS checks its cache for a stored IP address.
- DNS Resolver Query: If not found, the request is sent to a DNS resolver (usually by ISP).
- Root Server Query: The resolver queries a root server, which points to the correct TLD server.
- TLD Server Response: The TLD server directs the resolver to the domain’s authoritative server.
- Authoritative Server Response: The authoritative server returns the actual IP address.
- Final Response: The resolver sends the IP back to the user, and the browser connects to the server.

## Records
- A → IPv4         --> google.com → 142.x.x.x
- AAAA → IPv6
- CNAME → Alias    --> www.google.com → google.com
- MX → Mail        --> Used for email routing
- NS → Name server
- PTR → Reverse lookup