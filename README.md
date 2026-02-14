# VPN-Secure-File-Sharing-Implementation
Secure VPN and file sharing implementation using OpenVPN and Samba on Linux. Built a full PKI with Easy-RSA and configured TLS-encrypted tunneling between two remote environments. Verified secure, controlled file access exclusively through the encrypted VPN connection.

🔐 VPN & Secure File Sharing Implementation

Linux | OpenVPN | Samba

📌 Project Overview

This project demonstrates the implementation of a secure VPN tunnel between two geographically separated Linux virtual machines (US VM and Sri Lanka VM) using OpenVPN.

A complete Public Key Infrastructure (PKI) was built using Easy-RSA, and secure file sharing was configured using Samba over the encrypted VPN tunnel.

🌍 Architecture

US VM

OpenVPN Server

Samba File Server

Sri Lanka VM

OpenVPN Client

Communication between both environments is fully encrypted using TLS and certificate-based authentication.

🔐 Key Features

Secure site-to-site VPN using OpenVPN

Full PKI setup (CA, Server Certificate, Client Certificate)

HMAC protection using ta.key

TUN-based routing configuration

AES encryption with TLS authentication

Samba file server accessible only through VPN

Secure file operations verified over encrypted tunnel

🛠 Technologies Used

Linux (Ubuntu)

OpenVPN

EasyRSA (PKI Management)

Samba

TLS Encryption

tun Interfaces

Firewall Configuration (iptables)

📂 Implementation Steps
1️⃣ OpenVPN Server Setup

Installed OpenVPN & EasyRSA

Generated CA, server & client certificates

Generated Diffie-Hellman parameters

Created HMAC key

Configured server.conf

Enabled and started OpenVPN service

2️⃣ OpenVPN Client Setup

Transferred required certificates securely

Configured client profile (.ovpn)

Established secure VPN tunnel

Verified connection (tun0 interface, ping test)

3️⃣ Samba Configuration

Installed Samba server

Created shared directory

Configured smb.conf

Restarted Samba service

Verified secure file access through VPN

✅ Results

✔ VPN successfully established between US and Sri Lanka
✔ Secure TLS handshake completed
✔ tun0 interface created
✔ Successful ping between VPN endpoints
✔ Samba share accessible only via VPN
✔ File creation and directory listing verified

🎯 Learning Outcomes

Practical experience with VPN deployment

Understanding of PKI and certificate-based authentication

Secure routing and tunneling configuration

Linux server administration

Secure file sharing over encrypted networks

📌 Conclusion

This project successfully demonstrates the deployment of a secure OpenVPN infrastructure and controlled Samba file sharing across geographically separated Linux environments.

The system ensures confidentiality, integrity, and authenticated access to shared resources using encryption and certificate-based security.
