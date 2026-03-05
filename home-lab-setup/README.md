# Access Control Policy Documentation

## Project Overview

This project demonstrates the development of a structured **Access Control Policy** aligned with cybersecurity best practices and the **principle of least privilege**.

The objective is to define standards for user authentication, authorization, account lifecycle management, and privilege control within an organizational environment.

This project was created as part of a **cybersecurity home lab portfolio** to simulate how organizations design and implement **Identity and Access Management (IAM)** security policies.

---

## Technologies & Security Concepts

This project applies several core cybersecurity principles and frameworks:

- Identity and Access Management (IAM)
- Role-Based Access Control (RBAC)
- Multi-Factor Authentication (MFA)
- Least Privilege Principle
- Segregation of Duties
- Security Logging & Monitoring
- NIST Cybersecurity Framework
- CIS Security Controls
- CIA Triad (Confidentiality, Integrity, Availability)

---

## Purpose

The purpose of this policy is to ensure that access to systems, applications, and sensitive data is granted based on **business need**, **minimized risk exposure**, and **continuous monitoring** throughout the user lifecycle.

---

## Scope

This policy applies to:

- Employees
- Contractors
- Third-party vendors
- IT administrators
- All systems, applications, and network resources within the organization

---

## Policy Requirements

### 1. Account Provisioning

- All user accounts must be approved by management
- Access must be **role-based**
- Unique user IDs required (no shared accounts)
- Default passwords must be changed upon first login

### 2. Authentication Controls

- Minimum password length: **12 characters**
- Password complexity enforced
- **Multi-Factor Authentication (MFA)** for privileged accounts
- Account lockout after **5 failed login attempts**

### 3. Authorization & Least Privilege

- Access granted strictly based on **business need**
- Administrative privileges reviewed **quarterly**
- **Segregation of duties enforced**

### 4. Account Review Process

- Monthly review of privileged accounts
- Annual review of all user accounts
- Immediate **deprovisioning upon termination**

### 5. Logging & Monitoring

- Authentication attempts logged
- Privileged activity monitored
- Audit logs retained for **90 days**

---

## Risk Mitigation Impact

Proper access control reduces:

- Insider threat risk
- Privilege escalation
- Unauthorized data exposure
- Credential misuse
- Compliance failures

---

## Alignment With Security Frameworks

This policy aligns with:

- **NIST Cybersecurity Framework – Access Control (AC)**
- **CIS Critical Security Controls**
- **Principle of Least Privilege**
- **CIA Triad (Confidentiality, Integrity, Availability)**

---

## Future Improvements

- Active Directory integration
- Privileged Access Management (PAM)
- Single Sign-On (SSO)
- SIEM monitoring integration
- Automated identity lifecycle management

---

## Author

**Gisele Ribeiro**  
Cybersecurity Portfolio Project
