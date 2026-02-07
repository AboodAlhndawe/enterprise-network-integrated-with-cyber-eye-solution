# 🛡️ Cyber Eye  
**Rule-Based Intrusion Detection & Prevention System Integrated with a Honeypot**

---

## 📌 Project Overview
Cyber Eye is an integrated, real-time network threat monitoring platform that combines a **rule-based Intrusion Detection and Prevention System (IDS/IPS)** using **Suricata** with a **Honeypot (T-Pot)** deployed in a virtualized penetration testing environment (**PentLab**).

The project aims to enhance attack detection, improve security log analysis, and provide centralized visualization with automated alerts, enabling faster and more effective incident response.

---

## 🚨 Problem Statement
Modern networks face several security challenges, including:

- Frequent and persistent cyberattacks  
- Complex and fragmented security logs  
- Difficulty in real-time analysis and event correlation  
- Delayed attack detection and alert fatigue  

Cyber Eye addresses these challenges by providing:

- A unified platform for threat monitoring  
- Centralized log collection and analysis  
- Visual dashboards for security events  
- Automated real-time alerting  

---

## 🧠 System Overview
The system is composed of the following components:

- **Suricata IDS/IPS** operating in inline mode  
- **T-Pot Honeypot** for attracting and capturing real attacker behavior  
- **ELK Stack (Elasticsearch, Logstash, Kibana)** for log processing, analysis, and visualization  

### Working Process:
1. The Honeypot receives malicious traffic and attack attempts  
2. Attack behaviors and patterns are observed and analyzed  
3. Security rules are created and applied in Suricata  
4. Attacks are detected and optionally prevented in real time  

---

## 🎯 Target Audience
Cyber Eye is designed for:

- Security Operations Center (SOC) teams  
- Network administrators  
- Cybersecurity analysts  
- Cybersecurity students  

It is especially useful for environments that require:

- Real-time visibility into network attacks  
- Centralized security log analysis  
- Automated alerting and faster incident response  

---

## 🏗️ System Architecture

### Network Architecture & Traffic Flow
- All network traffic initially passes through **Suricata**  
- Legitimate traffic is forwarded to the Honeypots  
- Malicious traffic is:
  - Detected  
  - Logged  
  - Blocked (optionally)  

---

## 🔧 Suricata Configuration (Core Changes)
Key configuration adjustments include:

- Correcting `HOME_NET` to match the laboratory subnet  
- Enabling **EVE JSON logging**  
- Enabling **multi-threading**  
- Enabling **IP defragmentation**  

### Verification:
- Logs are successfully sent using **NFQUEUE**  
- Alerts and events are indexed in **Elasticsearch**  

---

## 🏁 Conclusion
Cyber Eye successfully delivers a comprehensive network threat monitoring solution by integrating:

- Honeypots  
- Intrusion Detection and Prevention  
- Centralized log processing  
- Real-time visualization and alerting  

The project provides a strong foundation for modern **Security Operations Centers (SOC)** and significantly improves the speed and effectiveness of responses to security incidents.

---

## 📚 References
- Suricata Official Documentation:  
  https://suricata.io/documentation/

- T-Pot Honeypot Platform (Deutsche Telekom Security):  
  https://github.com/telekom-security/tpotce

- Elasticsearch Documentation:  
  https://www.elastic.co/guide/index.html

- Kibana Documentation:  
  https://www.elastic.co/kibana/

- MITRE ATT&CK Framework:  
  https://attack.mitre.org/
