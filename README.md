# GitHub OSINT Minor Project

## 📖 Project Overview
This project demonstrates how **Open-Source Intelligence (OSINT)** techniques can be used to detect sensitive information leaks in public GitHub repositories.  
Using **Gitleaks**, we scanned the selected repository (`hashicorp/terraform`) and identified potential secret leaks.

---

## 🛠 Tools & Technologies Used
- **Gitleaks v8.28.0** – Secret scanning tool
- **GitHub Dorker (optional)** – Automated GitHub search for potential sensitive files
- **Kali Linux** – Penetration testing OS

---

## 📂 Repository Contents
- **report.json** → Output of Gitleaks scan showing detected secrets
- **project_report.pdf** → Detailed report with methodology and findings
- **README.md** → Project documentation

---

## 🔍 Project Methodology
1. **Environment Setup**
   - Installed Gitleaks from official GitHub release.
   - Configured GitHub Dorker (optional step).
2. **Target Selection**
   - Selected `hashicorp/terraform` repository as the test target.
3. **Secret Scanning**
   - Ran Gitleaks scan:
     ```bash
     gitleaks detect -s terraform -r report.json -f json
     ```
4. **Analysis & Reporting**
   - Analyzed detected secrets.
   - Documented methodology, findings, and recommendations.

---

## 📊 Key Findings
- **Total Secrets Detected:** 253
- **Types of Leaks Identified:**
  - API Keys
  - Cloud Provider Credentials
  - Configuration Secrets

---

## 🛡 Recommendations
- Remove hardcoded secrets and use environment variables.
- Implement GitHub secret scanning and CI/CD security checks.
- Regularly audit repositories for exposed credentials.

---

## 👤 Author
**Balaram Das**  
Email: bd9650576@gmail.com  

---

## 📜 License
This project is for **educational purposes only** and follows ethical hacking guidelines.
