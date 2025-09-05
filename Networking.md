🌐 Networking Cheat Sheet
Basic Protocols and Services
TCP vs. UDP
TCP: Reliable, connection-based. Used when data integrity is important (HTTP, SSH).

UDP: Fast, no delivery guarantee. Used when speed is important (streaming, DNS).

QUIC
A modern protocol over UDP that combines UDP's speed with TLS 1.3's reliability and security. Its key advantage is low latency and fixing "head-of-line blocking," which is critical for high-speed platforms.

Other Key Concepts
Routing: Finding the path for data packets.

Check with: traceroute, ip route show

Firewall: Controls network traffic.

Check with: ufw status, iptables -L

DNS: Translates a domain name into an IP address.

Diagnosis with: dig, nslookup

Security and Encryption (HTTPS/SSL/TLS)
HTTP: A protocol without encryption. HTTPS = HTTP + SSL/TLS.

SSL/TLS: A modern protocol for secure connections. SSL is an old standard, and TLS is its successor.

The "S" in HTTPS
The "S" stands for Secure. It guarantees three things:

Confidentiality: Data is encrypted.

Integrity: Data is not changed during transfer.

Authentication: A certificate proves the server is real.

Important Terms
TLS Handshake: The process of setting up a secure connection. Important: TLS 1.3 is faster than TLS 1.2.

Cipher Suites: A set of encryption algorithms. You should ensure that only strong and modern ones are used.

Certificate Pinning: A method where an app is linked to a specific certificate to protect against attacks.
