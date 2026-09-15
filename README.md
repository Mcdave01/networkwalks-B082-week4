# networkwalks-B082-week4
The mile stone project is done in week4
# 🔐 Mediroza Hospital Web Application Security Assessment

## Penetration Testing Laboratory Project

**Author:** Atanda Oluwagbenga  
**Platform:** Kali Linux  
**Project Type:** Authorized Cybersecurity / Penetration Testing Laboratory  
**Target:** Mediroza Hospital Lab Web Application

---

## ⚠️ Disclaimer

This project was performed in an authorized educational/laboratory environment.

The techniques documented in this repository are intended for cybersecurity education, penetration-testing practice, and systems for which explicit authorization has been granted.

Do not use these techniques against websites, servers, accounts, or applications without permission.

---

# 📖 Table of Contents

1. [Project Overview](#-project-overview)
2. [Objectives](#-objectives)
3. [Laboratory Environment](#-laboratory-environment)
4. [Methodology](#-methodology)
5. [Milestone 1 - Reconnaissance](#-milestone-1---web-reconnaissance)
6. [Milestone 2 - Web Application Discovery](#-milestone-2---web-application-discovery)
7. [Milestone 3 - PDF Hash Extraction](#-milestone-3---pdf-hash-extraction)
8. [Milestone 4 - Password Recovery](#-milestone-4---password-recovery-and-validation)
9. [Complete Attack/Testing Flow](#-complete-testing-flow)
10. [Findings](#-security-findings)
11. [Recommendations](#-security-recommendations)
12. [Lessons Learned](#-lessons-learned)
13. [Evidence](#-project-evidence)
14. [Repository Structure](#-repository-structure)
15. [Conclusion](#-conclusion)

---

# 📌 Project Overview

This project demonstrates a practical web application security assessment against the Mediroza Hospital laboratory environment.

The assessment follows a simplified penetration-testing methodology beginning with reconnaissance and continuing through application discovery, identification of protected documents, PDF hash extraction, controlled password recovery, and validation.

The project was completed through four major milestones:

```text
Milestone 1
     ↓
Web Reconnaissance

Milestone 2
     ↓
Web Application / Resource Discovery

Milestone 3
     ↓
PDF Hash Extraction

Milestone 4
     ↓
Password Recovery & Validation






🎯 Objectives

The objectives of this assessment were to:

Perform web reconnaissance.
Identify publicly available information.
Examine robots.txt.
Identify application directories.
Investigate the patient portal in the authorized lab.
Identify protected laboratory reports.
Download an encrypted PDF for analysis.
Extract a password-verification hash.
Perform controlled password recovery.
Validate the recovered password.
Identify security weaknesses.
Provide remediation recommendations.




🧰 Laboratory Environment
Operating System
Kali Linux
Tools
cURL
Web Browser
pdf2john
John the Ripper
PDF Viewer
GitHub
Basic Commands Used
curl

and password-recovery tools available in Kali Linux.

🔬 Methodology

The assessment followed this workflow:

Information Gathering
        ↓
Reconnaissance
        ↓
Resource Discovery
        ↓
Application Analysis
        ↓
Document Identification
        ↓
PDF Hash Extraction
        ↓
Controlled Password Recovery
        ↓
Password Validation
        ↓
Security Analysis
        ↓
Recommendations
        ↓
Documentation
















COMPLETE TESTING FLOW

The complete assessment can be summarized as follows:

1. Identify the web application
             ↓
2. Request robots.txt
             ↓
3. Identify /patient/, /staff/ and /old/
             ↓
4. Examine the authorized patient environment
             ↓
5. Identify laboratory reports
             ↓
6. Identify encrypted PDF documents
             ↓
7. Download an authorized test PDF
             ↓
8. Confirm that the PDF requires a password
             ↓
9. Extract the PDF password hash
             ↓
10. Prepare a controlled wordlist
             ↓
11. Perform dictionary-based password recovery
             ↓
12. Identify the weak password
             ↓
13. Enter the recovered password into the PDF viewer
             ↓
14. Successfully unlock the PDF
             ↓
15. Document security findings
             ↓
16. Provide remediation recommendations
📊 SECURITY FINDINGS
ID	Finding	Severity	Description
F-01	Application paths disclosed through robots.txt	Low	/patient/, /staff/, and /old/ were disclosed.
F-02	Sensitive laboratory reports	High	Medical reports require strong access controls.
F-03	Weak PDF password	High	The test password 123456 is highly predictable.
F-04	Offline password guessing risk	High	Obtaining an encrypted PDF can permit offline password testing.
F-05	Sensitive medical information	Critical	Patient information requires strong confidentiality protections.
🛡️ SECURITY RECOMMENDATIONS
1. Do Not Rely on robots.txt for Security

robots.txt should never be used to protect confidential directories.

Instead, implement:

Authentication
Authorization
Access Control
Server-side validation
2. Use Strong Passwords

The password:

123456

is extremely weak.

Users should use long and unique passwords.

Avoid:

123456
password
admin
12345678
qwerty
3. Implement Strong Authentication

Recommended controls include:

Strong password requirements
Multi-factor authentication
Login rate limiting
Account lockout controls
Secure session management
Secure password reset procedures
4. Implement Proper Authorization

A user should only be able to access documents they are authorized to access.

Authorization must be checked server-side for every request.

5. Protect Medical Documents

Sensitive reports should be protected through:

Encryption at rest
HTTPS/TLS
Strong authorization
Secure document storage
Temporary/signed download links
Access logging
Monitoring
6. Use Strong Password Protection

Where passwords are used by the application, modern password-hashing algorithms should be used.

Recommended options include:

Argon2id
bcrypt
scrypt
🧠 LESSONS LEARNED

This project provided practical experience with:

Reconnaissance

Understanding how publicly available information can reveal application structure.

Web Enumeration

Identifying application resources and understanding the importance of access controls.

Document Security

Understanding how password-protected PDF files protect sensitive documents.

Hash Extraction

Learning how encrypted documents can be prepared for controlled password analysis.

Password Security

Demonstrating the weakness of predictable passwords.

Dictionary Attacks

Understanding how password candidates can be tested against password-verification data.

Validation

Learning the importance of confirming a finding instead of relying solely on tool output.

Reporting

Learning how to document:

Evidence
↓
Observation
↓
Impact
↓
Risk
↓
Recommendation
📸 PROJECT EVIDENCE
Milestone 1 - Reconnaissance

The screenshot below demonstrates the robots.txt response and the application paths discovered.

Milestone 2 - Protected Reports

The screenshot demonstrates the laboratory reports available through the authorized environment.

Milestone 3 - PDF Hash

The screenshot demonstrates the extracted PDF password hash.

Milestone 4 - Password Recovery

The screenshot demonstrates the successful password-recovery result.

Password Validation

The recovered password was entered into the PDF viewer.

Recovered Laboratory Report

After successful password validation, the encrypted PDF was opened.

📁 REPOSITORY STRUCTURE

The final GitHub repository can be organized as:

mediroza-security-assessment/
│
├── README.md
│
├── screenshots/
│   ├── Capture-1.PNG
│   ├── Capture-2_after_being_cracked.PNG
│   ├── Capture-3_hash.PNG
│   ├── Capture-4_pdfCracked.PNG
│   ├── Capture-5_opening_the_Pdf.PNG
│   └── Capture-6_the_data.PNG
│
└── report/
    └── penetration-testing-report.pdf
📝 REPORTING FORMAT

For each vulnerability identified during the assessment, the following format was used:

Finding
   ↓
Evidence
   ↓
Technical Observation
   ↓
Potential Impact
   ↓
Severity
   ↓
Recommendation



⚖️ ETHICAL AND LEGAL CONSIDERATION

All testing documented in this project was performed within an authorized educational laboratory environment.

Penetration testing should only be performed when permission has been granted.

Unauthorized activities such as:

Password cracking
Vulnerability scanning
Directory enumeration
Exploitation
Unauthorized document access
Credential testing

may violate organizational policies and applicable laws.

🏁 CONCLUSION

The Mediroza Hospital security assessment demonstrated a complete introductory penetration-testing workflow.

The assessment began with basic reconnaissance:

robots.txt

which revealed application paths.

The assessment then progressed to:

Patient Portal
      ↓
Laboratory Reports
      ↓
Encrypted PDF
      ↓
PDF Hash Extraction
      ↓
Controlled Password Recovery
      ↓
Password Validation

