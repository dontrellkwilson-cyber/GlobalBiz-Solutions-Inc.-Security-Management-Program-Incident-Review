# GlobalBiz Solutions Inc. Security Management Program Incident Review

## Project Overview

This project presents a security management program review for **GlobalBiz Solutions Inc. (GBS)**, a fictional publicly traded international organization with offices and data centers in the United States, Europe, and Asia.

The assessment examines two significant cybersecurity incidents:

- A third-party vendor compromise that exposed the GBS network
- An executive spear-phishing attack that led to unauthorized remote access and payment fraud

The review identifies the security management deficiencies that contributed to both incidents and recommends program-level changes designed to prevent similar events.

---

## Project Objectives

- Identify weaknesses in GBS’s security management program.
- Evaluate third-party security and vendor network access.
- Review email, endpoint, and payment-security controls.
- Recommend changes to vendor-risk management.
- Develop a secure standard for external connections.
- Improve email filtering and endpoint application control.
- Strengthen payment verification and role-based training.
- Explain how each recommended change could prevent similar incidents.
- Align the recommendations with NIST guidance.

---

## Skills Demonstrated

- Security Program Evaluation
- Third-Party Risk Management
- Supply Chain Security
- Vendor Access Governance
- Firewall Policy Review
- Secure Network Connections
- Email Security
- Endpoint Application Control
- Application Allowlisting
- Payment Fraud Prevention
- Role-Based Security Training
- Phishing Simulation Planning
- Incident Prevention
- NIST Security Guidance

---

## Organization Profile

GlobalBiz Solutions Inc. is a publicly traded S&P 500 company headquartered in San Francisco.

The organization:

- Employs more than 10,000 people
- Operates 25 offices worldwide
- Maintains data centers in the United States, Europe, and Asia
- Processes personal and financial information
- Handles protected health information
- Uses payment-card systems
- Transfers data internationally
- Relies heavily on third-party vendors for infrastructure maintenance

Because GBS operates globally and depends on outside providers, its security management program must address both internal controls and third-party risk.

---

## Incident Summary

### Incident 1: Third-Party Vendor Compromise

A compromised toner vendor server used a trusted connection to transfer malicious tools into an internal GBS server.

The attack involved:

- Cobalt Strike
- Mimikatz
- Credential theft
- Unauthorized access
- Sensitive data leaving GBS
- Abuse of a trusted vendor connection

The incident was made possible by weak vendor oversight, broad firewall access, and outdated network protocols.

---

### Incident 2: Executive Spear Phishing and Payment Fraud

The vice president for client relations received a phishing email that appeared to come from an international client.

The executive installed TeamViewer, and the corporate purchase card later reached its $150,000 limit.

The incident exposed weaknesses in:

- Email filtering
- Software-installation permissions
- Endpoint monitoring
- Remote-access controls
- Payment approval
- Security training

---

## Security Management Deficiency 1: Third-Party Security and Network Access

GBS did not maintain sufficient controls over its vendors or the network access granted to them.

### Identified Weaknesses

- No defined minimum security requirements for vendors
- Generic bidirectional firewall rules
- Excessive trust in external connections
- Limited review of vendor security
- Broad access beyond business requirements
- Continued use of PPTP
- Unencrypted or outdated connections
- Limited monitoring of vendor activity

The problem extended beyond a single firewall rule. GBS allowed vendor access without consistently confirming that the vendor’s controls remained effective.

---

## Recommended Changes for Deficiency 1

### Change 1: Third-Party Security Risk Management Program

GBS should establish a formal third-party security risk management program before granting vendors access to company systems.

The review process should evaluate:

- The data the vendor will access
- The systems the vendor will use
- The network paths required
- The sensitivity of the information involved
- The vendor’s security controls
- The vendor’s incident-response capability
- The risk created by the connection

Vendor contracts should include:

- Minimum security requirements
- Breach-notification duties
- Cooperation during investigations
- Notification of major security changes
- Access restrictions
- Audit rights
- Corrective-action requirements

Each high-risk vendor should have an assigned owner. High-risk third parties should be reviewed at least annually, and corrective actions should be tracked to completion.

---

### Change 2: Vendor Connection Standard

Every external vendor connection should follow the same written security standard.

Each vendor should receive a separate firewall rule that permits only the required:

- Source addresses
- Destination systems
- Ports
- Protocols
- Services
- Business functions

All other traffic should be denied by default.

The standard should also:

- Prohibit PPTP
- Prohibit unencrypted connections
- Require approved encryption
- Require centralized key management
- Require scheduled firewall-rule reviews
- Require logging and monitoring
- Remove access when it is no longer needed
- Document all approved exceptions

---

## How the Deficiency 1 Changes Prevent Similar Incidents

### Third-Party Risk Management Program

Regular vendor reviews would prevent GBS from leaving access in place only because a company had been trusted in the past.

Security assessments and contract requirements would help identify weak controls before access is approved. Ongoing reviews would also detect changes in a vendor’s security posture and require corrections before access continues.

Clear breach-notification duties would help GBS respond more quickly when a vendor experiences a security incident.

---

### Vendor Connection Standard

Vendor-specific firewall rules would limit each connection to its approved purpose.

A compromised vendor server would be unable to:

- Reach unrelated systems
- Use unnecessary ports
- Transfer unauthorized tools
- Send credential data
- Exfiltrate information through unapproved paths

Deny-by-default controls would reduce the attack surface, while replacing PPTP with approved encryption would reduce the risk of credentials being exposed in transit.

---

## Security Management Deficiency 2: Email, Endpoint, and Payment Security

The second incident showed that GBS’s email, endpoint, and payment controls did not work together to stop the attack.

### Identified Weaknesses

- Weak external email filtering
- No effective impersonation detection
- Standard users could install software
- No application allowlisting
- TeamViewer was not blocked
- No automated endpoint alert
- Limited after-hours monitoring
- Payment validation was bypassed
- No second approval for unusual transactions
- Insufficient role-based phishing training

GBS had several opportunities to stop the attack, but the email, workstation, and payment controls all failed.

---

## Recommended Changes for Deficiency 2

### Change 1: Email and Endpoint Application Control Program

GBS should strengthen controls across both the email system and employee workstations.

The email system should:

- Label external messages
- Inspect links
- Inspect attachments
- Detect sender impersonation
- Quarantine suspicious messages
- Flag unusual refund or payment requests
- Alert on messages requesting software installation

Endpoint controls should:

- Remove local installation rights from standard users
- Use application allowlisting
- Block unapproved remote-access software
- Alert when prohibited software is downloaded
- Alert when prohibited software is installed
- Alert when prohibited software is executed
- Monitor outside normal U.S. business hours

Unapproved remote-access tools such as TeamViewer should be blocked by default.

---

### Change 2: Payment Verification and Role-Based Training

GBS should revise its refund and payment procedures.

Unusual payments, refunds, or new payment instructions should require:

- Verification through a known contact number
- Independent confirmation
- Approval by a second authorized employee
- Documented approval
- Escalation for high-value transactions

Executives and payment personnel should receive role-based training involving:

- Executive impersonation
- Refund fraud
- Payment redirection
- Remote-access scams
- Business email compromise
- Suspicious attachments and links
- Verification procedures

Employees should also participate in periodic phishing simulations. Anyone who fails a simulation or bypasses the payment process should complete follow-up training.

---

## How the Deficiency 2 Changes Prevent Similar Incidents

### Email and Endpoint Application Control

The attack would have to bypass several independent controls before TeamViewer could be used.

Possible prevention points include:

1. Email filtering quarantines the phishing message.
2. Impersonation detection flags the sender.
3. Installation restrictions prevent TeamViewer from being installed.
4. Application allowlisting blocks the program.
5. Endpoint monitoring alerts the SOC.
6. The workstation is isolated before further access occurs.

Using several layers makes it less likely that one failed control will lead directly to compromise.

---

### Payment Verification and Training

A fraudulent payment should not be completed based only on an email, phone call, or request from one employee.

Calling a known contact could reveal an impersonation attempt before funds are released. Secondary approval would prevent one compromised user from authorizing the transaction alone.

Role-based training and phishing simulations would help executives and payment personnel recognize suspicious requests and follow required procedures.

---

## Security Recommendations Summary

| Security Area | Recommended Improvement |
|---|---|
| Vendor Governance | Establish a formal third-party risk management program |
| Vendor Contracts | Add security, breach-notification, and investigation requirements |
| Vendor Assessments | Review high-risk vendors at least annually |
| Firewall Access | Use vendor-specific allow rules |
| Network Policy | Deny all unapproved traffic by default |
| Encryption | Prohibit PPTP and unencrypted vendor connections |
| Email Security | Detect impersonation and quarantine suspicious messages |
| Endpoint Security | Remove local installation rights |
| Application Control | Use application allowlisting |
| Remote Access | Block unauthorized tools such as TeamViewer |
| Monitoring | Alert the SOC and provide after-hours coverage |
| Payment Security | Require callbacks and secondary approval |
| Training | Provide role-based phishing education |
| Testing | Conduct recurring phishing simulations |

---

## Defense-in-Depth Approach

The recommended changes work best when implemented together.

### Vendor Incident Prevention

A stronger vendor program combines:

- Vendor assessments
- Security contract requirements
- Restricted firewall rules
- Approved encryption
- Continuous monitoring
- Scheduled access reviews

### Spear-Phishing Incident Prevention

A stronger anti-fraud program combines:

- Email filtering
- External-message labeling
- Application allowlisting
- Restricted installation rights
- Endpoint alerts
- Independent payment verification
- Role-based training

No single control is expected to stop every attack. Multiple layers reduce the chance that one failure will lead to a major incident.

---

## Project Files

Because this project is a written security management assessment, the repository does not require screenshots or an images folder.

Suggested repository structure:

```text
GlobalBiz-Security-Management-Incident-Review/
│
├── README.md
└── docs/
    └── GlobalBiz-Security-Management-Incident-Review.pdf
```

### Documentation

- **[Full Security Management Program Incident Review](https://github.com/user-attachments/files/30113801/GlobalBiz.Solutions.Inc.Task.3.docx)**
- **[D832 Case Study 5.pdf](https://github.com/user-attachments/files/30113800/D832.Case.Study.5.pdf)**

---

## Key Takeaways

The two incidents occurred through different attack methods, but both showed that GBS relied too heavily on trust and employee judgment.

The vendor compromise resulted from weak third-party oversight, broad network access, and outdated encryption. The spear-phishing incident succeeded because email, endpoint, remote-access, and payment controls did not stop the attack.

A formal vendor-risk program, restricted vendor connections, stronger email and endpoint controls, application allowlisting, independent payment verification, and role-based training would reduce the likelihood and impact of similar incidents.

---

## References

- Boyens, J., Smith, A., Bartol, N., Winkler, K., Holbrook, A., & Fallon, M. (2024). *Cybersecurity Supply Chain Risk Management Practices for Systems and Organizations*. NIST Special Publication 800-161 Revision 1, Update 1.
- Scarfone, K., & Hoffman, P. (2009). *Guidelines on Firewalls and Firewall Policy*. NIST Special Publication 800-41 Revision 1.
- Western Governors University. *D832 Case Study 5: GlobalBiz Solutions Inc.*

---

## Author

**Dontrell Wilson**  
Cybersecurity and Information Assurance Student  
CompTIA A+ | Network+ | Security+ | ITIL 4 Foundation
