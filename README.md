# PENETRATION TESTING REPORT
## FOOTPRINTING & NETWORK SCANNING - WEEK 2

**Name:** Ahmad
**Lab:** Kali Linux
**Target:** testphp.vulnweb.com (Intentionally Vulnerable Site), google.com, localhost

---

## 1. SELECTED MODULES

| Type | Module | Status |
| :--- | :--- | :--- |
| Elective | W2-PM1 - Footprinting with multiple Kali tools | Completed |
| Elective | W2-PM2 - GHDB based Footprinting Attacks | Completed |
| Mandatory | W2-PM5 - Zenmap based Network Scanning | Completed |
| Mandatory | W2-PM-FINAL - Detailed Report (This Report) | Completed |

Requirement was: Minimum 1 Elective + 2 Mandatory = 3 Modules. I completed 4 Modules.

---

## 2. W2-PM1 - FOOTPRINTING WITH MULTIPLE KALI TOOLS

### 2.1 Ping Test
**Result:** 2 packets transmitted, 2 received, 0% packet loss
rtt min/avg/max = 44.804 / 46.605 / 48.407 ms
**Conclusion:** Target is live and connection is stable.

### 2.2 Nmap on Localhost
**Step 1:**
Result: All 1000 scanned ports are closed.

**Step 2:**
Result: `8000/tcp open http SimpleHTTPServer 0.6 (Python 3.13.12)`
**Conclusion:** Nmap correctly detected closed port first, then open port after starting the server.

### 2.3 Nmap on testphp.vulnweb.com
This shows open ports, services and versions of the target.

---

## 3. W2-PM2 - GHDB / GOOGLE DORKING

This is Passive Footprinting.

| No. | Google Dork | What I Found |
| :--- | :--- | :--- |
| 1 | site:testphp.vulnweb.com filetype:pdf | PDF Report found |
| 2 | site:testphp.vulnweb.com inurl:login | login.php found |
| 3 | site:testphp.vulnweb.com inurl:admin | /admin/ found |
| 4 | site:testphp.vulnweb.com intitle:"index of" | No open directory found |
| 5 | site:testphp.vulnweb.com inurl:php?id= | listproducts.php?id= , artists.php?id= found |

**Conclusion:** With Google Dorking, an attacker can find login, admin and parameter pages without scanning.

---

## 4. W2-PM5 - ZENMAP BASED NETWORK SCANNING

Zenmap is the GUI version of Nmap.
- Opened Zenmap
- Target: testphp.vulnweb.com / 127.0.0.1
- Profile: Intense Scan / Service Version Scan selected
- Ran scan and checked Host Details and Topology

**Result:** Zenmap gave the same result as Nmap command line. GUI made it easier to understand.

---

## 5. OVERALL CONCLUSION

In this week, I learned both Passive (Google Dorking) and Active (Ping, Nmap, Zenmap) Footprinting. All work was done for learning purpose only, on an intentionally vulnerable lab site.

## 6. ETHICAL NOTE

Do not use these tools on any real website without written permission.
