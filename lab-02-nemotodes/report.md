# 🛡️ Incident Report – NEMOTODES Infection (Lab 2)

## 📌 Executive Summary

On November 26, 2024, a workstation inside the NEMOTODES.HEALTH environment was found compromised after connecting to a malicious domain associated with cracked software distribution. The infected host (`10.11.26.183`) executed network communications consistent with **NetSupport Remote Access Trojan (RAT)** activity.

The user `oboomwald` on host `DESKTOP-B8TQK49` triggered suspicious DNS requests, established external TLS connections, and communicated with a known command-and-control (C2) server. Internal SMB activity against the domain controller was also observed, indicating potential reconnaissance or lateral movement attempts.

---

## 👤 Victim Details

- **Hostname:** DESKTOP-B8TQK49  
- **IP Address:** 10.11.26.183  
- **MAC Address:** d0:57:7b:ce:fc:8b  
- **User Account:** oboomwald  
- **Domain:** NEMOTODES.HEALTH  

---

## 🔍 Attack Summary

The infection likely originated from a malicious download or site impersonating cracked software repositories.

Observed behavior includes:

- DNS query to malicious domain
- TLS communication to external infrastructure
- NetSupport RAT beaconing activity
- SMB connection attempts to internal domain controller (10.11.26.3)
- Suspicious HTTP POST traffic over non-standard usage patterns

---

## 🧠 MITRE ATT&CK Mapping

- T1566 – Phishing / Malicious Download
- T1105 – Ingress Tool Transfer
- T1071 – Application Layer C2 Communication
- T1021 – Remote Services (SMB)
- T1219 – Remote Access Software (NetSupport RAT)

---

## 📌 Conclusion

The host `10.11.26.183` is confirmed compromised with NetSupport RAT, allowing remote attacker control. Immediate isolation and blocking of associated IOCs is recommended.
