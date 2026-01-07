# Machine: Mr. Robot (VulnHub)

## Overview
- Platform: VulnHub
- Difficulty: Medium
- Objective: Obtain root access
- Environment: Local lab

## Disclaimer
This report is for educational purposes only.
All actions were performed on an intentionally vulnerable lab machine
in an authorized environment.

## Scope
- Target: Single vulnerable VM
- Network: Local NAT / Host-only
- Out of Scope: DoS attacks

## Methodology

### 1. Reconnaissance
Initial network scanning was conducted to identify open ports
and exposed services. A web service was discovered.

### 2. Enumeration
Web enumeration revealed a WordPress CMS.
User enumeration and directory discovery provided further insight.

### 3. Exploitation
An authenticated WordPress attack vector allowed remote code execution,
resulting in an initial low-privilege shell.

### 4. Post-Exploitation
Local enumeration identified misconfigured binaries
suitable for privilege escalation.

### 5. Privilege Escalation
A misconfigured SUID binary was abused to escalate privileges
and obtain root access.

## Proof of Access
Root access was successfully achieved.
Sensitive files and flags have been omitted.

## Tools Used
- Nmap
- Gobuster
- WPScan
- Netcat
- Linux enumeration tools

## Key Takeaways
- CMS misconfigurations are critical attack vectors
- Proper permission management is essential
- Regular security audits reduce risk

## Mitigations
- Harden CMS configurations
- Enforce least privilege
- Remove unnecessary SUID binaries
