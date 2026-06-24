# 🚨 Indicators of Compromise (IOCs)

## 🖥️ Victim Host

- IP Address: 10.11.26.183
- Hostname: DESKTOP-B8TQK49
- MAC Address: d0:57:7b:ce:fc:8b
- Username: oboomwald

---

## 🌐 Malicious Domains

- modandcrackedapk.com

---

## ☠️ Command & Control (C2)

- 194.180.191.64 (NetSupport RAT C2)
- 193.42.38.139 (TLS / hosting infrastructure)

---

## ⚠️ Observed Malicious Behavior

- NetSupport RAT check-in activity
- DNS requests to malicious domains
- TLS 1.0 insecure connections
- SMB traffic to internal domain controller (10.11.26.3)
- HTTP POST traffic on unusual ports

---

## 🧠 Notes

All IOCs indicate a remote access trojan infection with external command-and-control communication.
