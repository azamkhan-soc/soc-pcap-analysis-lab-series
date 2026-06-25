# 🛡️ Indicators of Compromise – Lab 03

## 🖥️ Infected Host
172.16.1.66 (DESKTOP-SKBR25F)

## 🧑 Domain Controller
172.16.1.4 (WIRESHARK-WS-DC)

---

## 🌐 External IPs Observed
13.69.239.79
20.96.153.111
52.109.6.53
23.52.9.222
40.126.29.14
204.79.197.203
199.232.196.209
140.82.113.3
185.199.110.133

---

## 🌍 Domains Observed
wiresharkworkshop.online
github.com
objects.githubusercontent.com
repo1.maven.org
msn.com
bing.com
officeclient.microsoft.com
login.microsoftonline.com
go.microsoft.com
wpad.wiresharkworkshop.online

---

## 🔐 Suspicious TLS Activity (SNI)
v20.events.data.microsoft.com
mobile.events.data.microsoft.com
odc.officeapps.live.com
config.edge.skype.com
autodiscover-s.outlook.com
img-s-msn-com.akamaized.net

---

## 📌 Notes
- High volume of Microsoft telemetry domains
- External code repository access (GitHub + Maven)
- Possible malware staging or C2 communication pattern
