# IAM Access Control Lab

## Project Overview

This project demonstrates basic Identity and Access Management (IAM) concepts, including user access, role-based permissions, least privilege, access reviews, onboarding, and offboarding.

The goal of this lab is to show how organizations can manage user access securely and make sure employees only have the permissions they need to perform their job.

## Skills Practiced

- Identity and Access Management (IAM)
- Least privilege
- Role-based access control (RBAC)
- User onboarding and offboarding
- Access review documentation
- Security documentation
- Risk awareness
- Basic compliance thinking

## Scenario

A small company has employees in different departments. Each employee needs access only to the systems and folders required for their role.

The company wants to reduce security risk by making sure users do not have unnecessary access.

## User Access Table

| User Role | Access Needed | Group Assigned | Risk Level |
|---|---|---|---|
| HR Employee | Employee records | HR-ReadOnly | High |
| IT Support | Ticketing system and device support tools | IT-Support | Medium |
| Finance Employee | Invoices and payment records | Finance-ReadOnly | High |
| Manager | Team reports and approvals | Manager-Access | Medium |
| Contractor | Temporary project folder only | Contractor-Temp | Medium |

## Access Control Rules

1. Users should only receive access required for their job.
2. High-risk access should require manager approval.
3. Contractor access should have an expiration date.
4. Admin access should be limited to authorized IT staff.
5. Access should be reviewed regularly.
6. Access should be removed immediately when someone leaves the company.

## Onboarding Checklist

When a new employee joins the company:

- Confirm employee name, department, and manager.
- Identify the systems and folders needed for the role.
- Assign the user to the correct group.
- Avoid giving extra access.
- Document who approved the access.
- Confirm the user can log in successfully.

## Offboarding Checklist

When an employee leaves the company:

- Disable the user account.
- Remove the user from all groups.
- Revoke access to shared folders and systems.
- Remove VPN or remote access if applicable.
- Document the date and time access was removed.
- Confirm with the manager that access is no longer needed.

## Access Review Checklist

During an access review:

- Review users with admin access.
- Check if contractors still need access.
- Remove users from groups they no longer need.
- Confirm high-risk access is approved.
- Document any changes made.
- Follow up with managers when access is unclear.

## Example Risk Findings

| Finding | Risk | Recommendation |
|---|---|---|
| Contractor account has no expiration date | Unauthorized access after project ends | Set an expiration date |
| Finance user has access to HR files | Data privacy risk | Remove unnecessary access |
| Too many users have admin access | Higher chance of misuse or mistake | Limit admin access |
| Former employee account still active | Security breach risk | Disable account immediately |

## What I Learned

This project helped me understand how IAM supports cybersecurity by controlling who has access to company systems and data.

I learned that access should be based on job role, business need, and least privilege. I also learned that onboarding, offboarding, and access reviews are important parts of protecting an organization.

## How This Applies to a Cybersecurity Role

This project connects to IAM, GRC, SOC, and IT security roles because access control is a key part of protecting systems and sensitive data.

In a real cybersecurity environment, IAM helps prevent unauthorized access, reduce insider risk, support compliance, and protect company information.
