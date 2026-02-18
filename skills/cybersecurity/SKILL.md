# Cybersecurity & Hacking Skill

Professional security posture with offensive and defensive capabilities.

## Offensive Security (Hacking)

### Reconnaissance
- **Passive**: WHOIS, DNS, social media
- **Active**: Port scanning, banner grabbing
- **Tools**: Nmap, Shodan, Censys, Maltego

### Network Exploitation
- **Scanning**: Nmap, Masscan
- **Enumeration**: Enum4linux, SNMPwalk
- **Exploitation**: Metasploit, Empire, Cobalt Strike
- **Post-exploitation**: Mimikatz, BloodHound

### Web Application
- **OWASP Top 10 2025**:
  1. Broken Access Control
  2. Cryptographic Failures
  3. Injection (SQL, NoSQL, Command)
  4. Insecure Design
  5. Security Misconfiguration
  6. Vulnerable Components
  7. Auth Failures
  8. Data Integrity Failures
  9. Logging Failures
  10. SSRF

- **Tools**: Burp Suite, SQLMap, Nikto, Gobuster

### Wireless & Physical
- **WiFi**: Aircrack-ng, Wifite
- **RF**: HackRF, SDR tools
- **Physical**: Rubber Ducky, LAN Turtle

## Defensive Security

### Detection & Monitoring
- **SIEM**: Splunk, ELK Stack, Sentinel, Chronicle
- **EDR**: CrowdStrike, SentinelOne, Carbon Black
- **Threat Intel**: MISP, Anomali, ThreatConnect

### Incident Response
```
1. Preparation
2. Identification
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned
```

### Blue Team Operations
- Log analysis
- Network monitoring
- Threat hunting
- Malware reverse engineering

## Secure Coding

### Input Validation
```python
# Never trust user input
def sanitize_input(user_input):
    # Whitelist validation
    allowed = re.compile(r'^[a-zA-Z0-9]+$')
    if not allowed.match(user_input):
        raise ValueError("Invalid input")
    return user_input
```

### Parameterized Queries
```python
# Prevent SQL injection
cursor.execute("SELECT * FROM users WHERE id = %s", (user_id,))
```

### Secret Management
```python
# Environment variables, not code
import os
api_key = os.getenv("API_KEY")
if not api_key:
    raise ValueError("API_KEY not set")
```

## Vulnerability Assessment

### Automated Scanning
- Nessus - vulnerability scanner
- OpenVAS - open source scanner
- Nessus - commercial
- Qualys - continuous scanning

### Manual Testing
- Code review (SAST)
- Penetration testing
- Configuration review
- Social engineering testing

## Multi-Agent Security

```
Kimi: Threat analysis, incident response
GLM5: Deep vulnerability research, reverse engineering
MiniMax: Scan automation, quick assessment, CVE matching

Delegation:
- Pentest scope → GLM5
- CVE analysis → MiniMax
- Incident response → Direct
```

## Commands

- `/scan` - Vulnerability scan
- `/analyze` - Security analysis
- `/pentest` - Penetration testing plan
- `/harden` - Security hardening
- `/incident` - Incident response
- `/threat` - Threat assessment

## Certifications
- CEH (Certified Ethical Hacker)
- OSCP (Offensive Security)
- CISSP (Management)
- Security+
