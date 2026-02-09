# SSH Brute Force Detection using Elastic SIEM

## Project Overview
This project demonstrates the detection, investigation, and response to an SSH brute force attack using Elastic SIEM in a controlled/isolated lab environment.The goal is to simulate a real-world attack scenario, generate security alerts, analyze attacker behavior, and apply SOC-style incident response techniques.

### Lab Environment
- OS: Ubuntu Linux (Virtual Machine)
- SIEM: Elastic Stack (Elasticsearch, Kibana, Elastic Agent)
- Log Source: System logs (auth.log)
- Attack Type: SSH Brute Force


##  Attack Scenario
An external attacker attempted multiple SSH login attempts using invalid credentials against a Linux host, triggering security alerts in Elastic SIEM.

## Detection & Alerting
-Alert Name: SSH Brute Force Attempt
-Severity: Medium
-Host: ubuntuopenfhe
-Event Type: Multiple failed SSH login attempts
-Framework: MITRE ATT&CK
-Tactic: Credential Access
-Technique: Brute Force
-Sub-technique: Password Guessing (T1110)

## Investigation Process
Multiple failed SSH authentication attempts observed
No successful login detected
No privilege escalation activity observed
Attack classified as attempted intrusion, not a successful breach

## MITRE ATT&CK Mapping
Tactic:Credential Access
- Technique:Brute Force
- Sub-technique:Password Guessing
- Technique id:110

## Findings
- Successful Login:No successful SSH login was detected
- Privilege Escalation:No evidence of privilege escalation was identified.
- No suspicious activity related to: **sudo**usage and **su** commands
- Impact Level:Medium to High

## Response & Mitigation
-Block attacker IP using firewall (UFW / iptables)
-Enable SSH rate-limiting
-Enforce strong password policies
-Use SSH key-based authentication
-Monitor IP reputation via threat intelligence
-Configure alert escalation for repeated attempts
## Lessons Learned
Importance of centralized log monitoring
Early detection prevents successful compromise
SIEM alerts must be correlated with log evidence
MITRE mapping helps standardize incident analysis
Documentation is critical for SOC operation
## Future Enhancements
Automate IP blocking via SOAR playbooks
Add geo-location analysis of attacker IPs
Integrate threat intelligence feeds
Expand detection to other attack techniques (Privilege Escalation, Persistence)
## Conclusion and Author
This project simulates real world SOC Level 1 activities including monitoring, alert triage, investigation, and security recommendations.
**Sarath Pulicherla
Aspiring SOC Analyst | Cybersecurity Enthusiast
GitHub: https://github.com/Sarath-Pulicherla**

