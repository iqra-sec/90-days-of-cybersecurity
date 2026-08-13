

# Day 01 — Linux & Network Service Lab

Date: 14 August 2026

Objective

Set up a basic Linux security lab using Kali Linux in Oracle VirtualBox and investigate a locally running network service.

## Environment

- Kali Linux
- Oracle VirtualBox
- Python 3
- Nmap

## Hands-On Work

### 1. Started a Python HTTP Server

I started a temporary HTTP server on port `8000` using:

```bash
python3 -m http.server 8000
The server reported that it was listening on 0.0.0.0:8000.
2. Inspected Listening Ports

I used:

ss -tuln

The output showed TCP port 8000 in the LISTEN state.

3. Scanned the Localhost

I then used Nmap to check port 8000:

nmap -p 8000 127.0.0.1

Nmap reported:

8000/tcp open http-alt

This confirmed that the HTTP service was reachable through the local interface.

Evidence
Socket Inspection
Key Takeaways
A running network service can listen on a specific TCP/UDP port.
ss can be used to inspect listening network sockets.
Nmap can be used to verify whether a port is exposed/open.
Running services contribute to a system's attack surface.
127.0.0.1 refers to the local host.
Next Steps
Learn Linux filesystem structure and permissions.
Understand TCP/IP and common network services.
Continue documenting hands-on security labs
