# 🔐 Security Implications of Cloud Misconfigurations in AWS

![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Security](https://img.shields.io/badge/Security-Research-red?style=for-the-badge)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📄 Overview

This repository contains the dissertation titled **"Security Implications of Cloud Misconfigurations in Amazon Web Services (AWS)"**, authored by **Umesh Udayan** (2025).

The research investigates how common misconfigurations in **Amazon S3** and **EC2** services can be identified, exploited, and mitigated through ethical penetration testing in a controlled AWS Free Tier environment.

---

## 🎯 Research Objectives

- Analyse common misconfiguration patterns in AWS S3 and EC2 services
- Simulate real-world attack scenarios using ethical penetration testing techniques
- Map findings to the **OWASP Top Ten** vulnerability categories
- Propose practical mitigation strategies grounded in AWS security frameworks
- Raise awareness among cloud administrators and cybersecurity professionals

---

## 🧪 Tests Conducted

| Test | Description | OWASP Mapping |
|------|-------------|---------------|
| Test 1 | S3 Public Listing and Read Access | A01, A05 |
| Test 2 | S3 Bucket Misconfiguration (Write Access) | A05 |
| Test 3 | EC2 Apache2 Sensitive File Exposure | A05, A02 |
| Test 4 | EC2 Metadata (IMDSv1) Exposure | A05, A07 |
| Test 5 | IAM Role Metadata Credential Extraction | A01, A05 |

---

## 🛠️ Tools Used

- **AWS CLI** – Resource provisioning, enumeration, and access testing
- **curl** – HTTP requests to EC2 metadata endpoints (IMDS)
- **SSH** – Secure connection to EC2 instances
- **Kali Linux** – Testing host environment
- **Web Browser** – Unauthenticated access validation

---

## 🏗️ AWS Environment

- **Services:** Amazon S3, Amazon EC2 (Apache2), IAM Roles
- **Region:** us-east-1
- **Network:** Default VPC
- **Instance Type:** t2.micro (Free Tier)
- **Testing Host:** Kali Linux Virtual Machine

---

## 📚 Frameworks & Standards Referenced

- [OWASP Top Ten 2021](https://owasp.org/Top10/)
- [AWS Well-Architected Framework – Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [CIS AWS Foundations Benchmark](https://www.cisecurity.org/benchmark/amazon_web_services)
- [NIST SP 800-115](https://csrc.nist.gov/publications/detail/sp/800-115/final)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

---

## 🔎 Real-World Case Studies Referenced

| Organisation | Year | Vulnerability |
|---|---|---|
| Capital One | 2019 | SSRF + IMDSv1 credential theft |
| Accenture | 2017/2021 | Public S3 bucket exposure |
| Toyota | 2022 | S3 misconfiguration – source code leak |
| US Department of Defense | 2023 | Open cloud storage – military emails |

---

## 🔒 Key Findings

- **S3 misconfigurations** led to direct public access to sensitive files without authentication
- **IMDSv1 exploitation** enabled extraction of temporary IAM credentials
- **Chained attacks** (metadata → credentials → S3 access) demonstrated the dangers of combining misconfigurations
- Simple configuration oversights can expose organisations to disproportionate risk

---

## 🛡️ Mitigation Recommendations

- ✅ Enable **S3 Block Public Access** at account and bucket level
- ✅ Enforce **IMDSv2** across all EC2 instances
- ✅ Apply **least privilege** IAM policies
- ✅ Enable **AWS CloudTrail** and **GuardDuty** for continuous monitoring
- ✅ Use **AWS Config** and **Security Hub** for automated drift detection
- ✅ Implement **Infrastructure as Code (IaC)** security scanning (e.g., Checkov)

---

## ⚖️ Ethical Considerations

All testing was conducted exclusively within a **personal AWS Free Tier account** using isolated, non-production environments. No third-party data, systems, or networks were accessed at any stage. The study received **formal ethical approval** from the university and complies with:

- UK Cyber Security Council Code of Ethics
- AWS Acceptable Use Policy
- GDPR and UK Data Protection Act 2018
- ACM Code of Ethics

---

## 📁 Repository Contents
