# Application Security Testing using OWASP ZAP

## Project Overview

This project demonstrates practical implementation of Dynamic Application Security Testing (DAST) using OWASP ZAP on a containerized web application deployed in a cloud environment.

The project combines:

- Cloud infrastructure provisioning (AWS EC2)
- Docker-based application deployment
- Runtime vulnerability assessment
- Security analysis and documentation

---

## 1. Cloud Infrastructure Provisioning

- Launched a virtual machine using Amazon Web Services (AWS) EC2 to host a web application
- Selected appropriate instance configuration
- Configured Security Group rules to allow:
  - SSH access (Port 22) for remote administration
  - HTTP traffic (Port 80) for application access
- Verified connectivity to the instance using SSH
- Confirmed proper network configuration before deploying the application
- Understood how cloud infrastructure components (instance, public IP, security groups) work together to securely host applications

---

## 2. Containerized Application Deployment

- Installed and configured Docker on the EC2 instance
- Pulled and deployed the intentionally vulnerable application OWASP Juice Shop as a Docker container
- Exposed the application on port 3000
- Mapped container ports to the host machine
- Verified successful deployment by accessing the application via the EC2 public IP address

### Practical Concepts Gained

- Container lifecycle management
- Port mapping and networking
- Running applications in isolated container environments

---

## 3. Dynamic Application Security Testing (DAST)

- Performed runtime security assessment using OWASP ZAP
- Configured the target URL in OWASP ZAP
- Conducted automated spidering to discover application endpoints
- Executed active scanning to detect vulnerabilities and HTTP misconfigurations
- Analyzed request/response cycles to identify potential attack vectors

Understood how DAST tools simulate attacker behavior to find runtime vulnerabilities without requiring access to source code.

---

## 4. Vulnerability Identification and Analysis

- Reviewed scan results and categorized alerts based on severity levels (Low, Medium, High)
- Analyzed confidence ratings for identified findings
- Identified missing HTTP security headers such as:
  - Content Security Policy (CSP)
  - X-Frame-Options
  - X-Content-Type-Options
- Observed additional informational findings related to:
  - Server configuration disclosures
  - Timestamp exposure
  - Cross-domain policy observations
- Analyzed how missing security headers increase risk exposure (e.g., clickjacking, MIME-type sniffing)

Developed understanding of how security misconfigurations are detected during dynamic testing.

---

## 5. Documentation and Learning Outcomes

- Documented scan findings and summarized identified vulnerabilities
- Gained hands-on experience deploying and testing a web application in a cloud-hosted environment
- Improved understanding of:
  - Cloud-based application hosting
  - Containerized deployment models
  - Practical DAST methodology
  - Common web security misconfigurations

---

## Project Summary

This project demonstrates practical exposure to:

- Cloud infrastructure deployment
- Docker-based application hosting
- Dynamic Application Security Testing (DAST)
- Vulnerability identification and security analysis
