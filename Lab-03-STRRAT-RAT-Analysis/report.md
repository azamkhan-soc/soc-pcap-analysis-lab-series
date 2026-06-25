# 🛡️ Lab 03 – STRRAT Malware Infection Analysis

## 🔥 Incident Summary
This investigation analyzed a PCAP file from a simulated enterprise network environment. The analysis confirmed that the endpoint **DESKTOP-SKBR25F (172.16.1.66)** was infected with **STRRAT Remote Access Trojan (RAT)**.

The malware was delivered via a malicious Java archive (JAR file) and established post-infection command-and-control (C2) communication with an external server.

---

## 🖥️ Victim Details

- Hostname: DESKTOP-SKBR25F  
- IP Address: 172.16.1.66  
- MAC Address: 00:1e:64:ec:f3:08  
- User Account: ccollier  
- Domain: wiresharkworkshop.online  
- Domain Controller: 172.16.1.4  

---

## ⚠️ Infection Details

- Malware: STRRAT RAT
- Delivery Method: Email attachment (JAR file)
- SHA256: 4c249b325125235b50d9690560c4197a28fd62901b5e02d9eba7436b29447cdd
- File Name: PL#40704.jar

---

## 🌐 Command & Control (C2)

- C2 Server: 141.98.10.69
- Port: 12132 (TCP)
- Behavior: STRRAT beaconing / ping communication observed in TCP stream

---

## 📡 Indicators of Compromise (IOCs)

### Internal Hosts
- 172.16.1.66 – Infected endpoint
- 172.16.1.4 – Domain Controller

### External IPs
- 141.98.10.69 (C2 Server)
- 13.69.239.79
- 20.96.153.111
- 204.79.197.203

### Domains Observed
- github.com
- objects.githubusercontent.com
- repo1.maven.org
- ip-api.com
- login.microsoftonline.com

### Malware Artifacts
- PL#40704.jar
- STRRAT beacon traffic (“ping” communication)

---

## 🧠 Conclusion

The host **DESKTOP-SKBR25F** was confirmed to be infected with STRRAT malware. Post-infection traffic indicates active command-and-control communication with an external attacker-controlled server.

### Final Verdict:
**Confirmed malware infection (STRRAT RAT compromise)**

Recommended actions:
- Isolate host
- Perform forensic analysis
- Block C2 IP (141.98.10.69)
- Review email delivery logs
