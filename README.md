# 🔒 Task 8 – VPN Setup & Privacy Protection

![Internship](https://img.shields.io/badge/Elevate%20Labs-Cybersecurity%20Internship-blue?style=for-the-badge)
![Tool](https://img.shields.io/badge/Tool-ProtonVPN-6D4AFF?style=for-the-badge&logo=protonvpn&logoColor=white)
![Protocol](https://img.shields.io/badge/Protocol-WireGuard-88171A?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## 📌 Objective

Set up a VPN, verify it successfully masks IP address and encrypts traffic, measure the real-world impact on network performance, and understand how VPN technology protects privacy.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **ProtonVPN** (Free Tier) | VPN client |
| **WhatIsMyIPAddress.com** | IP address verification before/after |
| **Speedtest.net** | Network speed comparison |
| **WireGuard Protocol** | VPN encryption |

---

## 🧪 Step-by-Step Process

| Step | Action | Result |
|------|--------|--------|
| 1 | Signed up for ProtonVPN Free Tier | Account created |
| 2 | Installed ProtonVPN on Windows | WireGuard configured |
| 3 | Checked IP before VPN | India, ISP visible |
| 4 | Connected to Norway server (NO-FREE#1) | Status: Protected |
| 5 | Checked IP after VPN | Oslo, Norway — ISP: Proton AG |
| 6 | Browsed Google via VPN tunnel | HTTPS traffic encrypted |
| 7 | Speed test with VPN active | Results recorded |
| 8 | Disconnected VPN | Status: Unprotected |
| 9 | Speed test without VPN | Baseline recorded |

---

## 📊 VPN Performance Comparison

| Metric | Without VPN | With VPN | Impact |
|--------|------------|---------|--------|
| **Download Speed** | 32.39 Mbps | 2.73 Mbps | ⬇️ -91.6% |
| **Upload Speed** | 48.79 Mbps | 14.80 Mbps | ⬇️ -69.7% |
| **Ping Latency** | 36 ms | 279 ms | ⬆️ +243 ms |
| **IP Address** | Real (India) | 205.147.17.2 | ✅ Masked |
| **Location** | India | Oslo, Norway | ✅ Changed |
| **ISP Visibility** | Visible | Hidden (VPN) | ✅ Protected |
| **Traffic Encryption** | ❌ No | ✅ WireGuard | ✅ Secured |

---

## 🛡️ VPN Features Verified

| Feature | Status | Notes |
|---------|--------|-------|
| IP Masking | ✅ Working | Websites see only VPN IP |
| Location Privacy | ✅ Working | Appears as Oslo, Norway |
| WireGuard Encryption | ✅ Strong | ChaCha20 + ECDH + Poly1305 |
| DNS Leak Protection | ✅ Working | Queries routed through VPN |
| HTTPS Support | ✅ Strong | Doubly encrypted |
| Server Load | ⚠️ 87% | Congested — free tier |

---

## 🔐 How WireGuard Encryption Works

```
1. Client initiates connection to VPN server
2. ECDH key exchange establishes shared secret
3. ChaCha20 encrypts all packets with shared key
4. Poly1305 authenticates each packet for integrity
5. ISP sees only encrypted gibberish
6. Websites see only VPN server IP (Norway)
```

| Component | Role |
|-----------|------|
| **ChaCha20** | Symmetric encryption of all traffic |
| **ECDH** | Secure key exchange |
| **Poly1305** | Packet authentication / integrity check |
| **UDP** | Transport protocol (faster than TCP) |

---

## ✅ VPN Benefits Demonstrated

- **IP Masking** — Real IP completely hidden from websites and ISPs
- **Traffic Encryption** — WireGuard encrypts all data end-to-end
- **ISP Monitoring Prevention** — ISP cannot see browsing history or DNS queries
- **Public WiFi Protection** — Safe to use on untrusted networks
- **Geographic Freedom** — Appears to browse from a different country

---

## ⚠️ VPN Limitations Identified

- **91.6% speed drop** — Free tier + international routing + server congestion
- **High latency (279ms)** — Not suitable for gaming or video calls
- **Trust model** — VPN provider can still see your traffic; requires trust in no-logs policy
- **Incomplete anonymity** — Doesn't prevent cookies, fingerprinting, or account tracking
- **No protection against** — Malware, phishing, or endpoint vulnerabilities

---

## 📸 Screenshots

All screenshots are in the [`/screenshots`](./screenshots) folder:

| File | Description |
|------|-------------|
| `01_protonvpn_signup.png` | ProtonVPN account setup |
| `02_protonvpn_installed.png` | Client installed on Windows |
| `03_ip_before_vpn.png` | Original IP — India |
| `04_vpn_connected.png` | Connected to Norway server |
| `05_ip_after_vpn.png` | New IP — Oslo, Norway |
| `06_browsing_via_vpn.png` | Browsing through VPN tunnel |
| `07_speedtest_with_vpn.png` | Speed test with VPN active |
| `08_vpn_disconnected.png` | VPN disconnected |
| `09_speedtest_without_vpn.png` | Speed test without VPN |

---

## 🧠 Key Learnings

- How VPN tunneling and encryption work in practice
- Real-world performance cost of VPN encryption and routing
- WireGuard protocol components and how they work together
- How to verify IP masking and DNS leak protection
- Why VPNs alone don't guarantee complete anonymity
- How to evaluate VPN services and their limitations

---

## 📁 Repository Structure

```
Cybersecurity-Internship-Task-8/
├── README.md
└── screenshots/
    ├── 01_protonvpn_signup.png
    ├── 02_protonvpn_installed.png
    ├── 03_ip_before_vpn.png
    ├── 04_vpn_connected.png
    ├── 05_ip_after_vpn.png
    ├── 06_browsing_via_vpn.png
    ├── 07_speedtest_with_vpn.png
    ├── 08_vpn_disconnected.png
    └── 09_speedtest_without_vpn.png
```
---

> 🔒 *This VPN setup was performed on a personal machine for educational purposes only as part of the Elevate Labs Cybersecurity Internship.*
