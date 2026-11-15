# PENETRATION TESTING REPORT
## FOOTPRINTING & NETWORK SCANNING PHASES
### W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS

| Field | Detail |
| :--- | :--- |
| **Pentester Name** | Ahmad Raza |
| **GitHub** | Ghallu305 |
| **University** | Virtual University |
| **Program/Batch** | B084 - NetworkWalks |
| **Date** | 15 November 2026 |
| **Modules Completed** | W2-PM1 - Multiple Kali Tools; W2-PM5 - Zenmap Scanning |
| **Client/Target** | 1. testphp.vulnweb.com (instructor-authorized educational exercise) 2. 127.0.0.1 - Own localhost |
| **Permission Secured?** | Instructor approval for the assigned domain exercise; own localhost for local scanning |
| **Phases Covered** | Phase 1: Reconnaissance & Footprinting; Phase 2: Scanning & Network Discovery |

## 1. Liability Disclaimer
I have performed these activities only on systems and networks that were within the authorized scope of my educational exercises or that I personally own or control.

The activities documented in this report were conducted for educational and cybersecurity learning purposes as part of the NetworkWalks program.

The footprinting exercise against testphp.vulnweb.com was performed with instructor approval. The Zenmap network scanning exercise was performed on my own localhost.

No exploitation, unauthorized access, or intentional disruption of services was performed.

## 2. Introduction
This report covers the practical cybersecurity activities completed during Week 2 of the NetworkWalks Cybersecurity & Ethical Hacking program.

The project focuses on two main areas:

**W2-PM1 - Footprinting and Reconnaissance Using Multiple Kali Linux Tools**
This module involved using Kali Linux tools to collect publicly observable information about the target domain.

**W2-PM5 - Network Scanning with Zenmap**
This module involved using Zenmap on Kali Linux to discover live hosts, identify open ports, and perform service version detection.

## 3. Tools Used
| Tool | Purpose |
| :--- | :--- |
| Kali Linux | Operating system used for footprinting activities |
| Zenmap / Nmap | Network scanning, host discovery, service detection |
| Nmap -sV | Service version detection |
| Python http.server | To start a local test web service on port 8000 |

## 4. Methodology

### 4.1 External Scan - testphp.vulnweb.com
Command Used:
