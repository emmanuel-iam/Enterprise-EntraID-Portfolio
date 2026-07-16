<h2>🏢Enterprise-EntraID-Portfolio

  ## Business-Scenario
  AccessShield Technologies is a growing technology and consulting company with employees working from offices in New York, New Jersey, Atlanta, and remotely across the United States.

The company recently hired 50 employees across Information Technology, Human Resources, Finance, Sales, Operations, and Executive Leadership. AccessShield Technologies currently relies on several manual processes for creating accounts, assigning access, managing employee transfers, and disabling accounts when workers leave the company.

Manual processes will created several business and security problems:

 - New employees sometimes wait too long to receive system access.
 - Users may receive access that does not match their job responsibilities.
 - Employees who transfer departments may keep access from their previous roles.
 - Contractors may remain active after their contracts expire.
 - Administrator accounts may have more privileges than necessary.
 - Managers have limited visibility into who has access to company applications.
 - Audit evidence is difficult to collect.
 - User onboarding and offboarding require too much manual work.

The leadership team has asked the Identity and Access Management team to design and implement a secure Microsoft Entra ID environment.

The new IAM solution must support the following business objectives:

  1. Create and manage 50 employee identities in Microsoft Entra ID.
  2. Organize users by department, job function, employee type, manager, and location.
  3. Automate access assignments using security groups, dynamic groups, and role-based access control.
  4. Require multifactor authentication for employees and administrators.
  5. Apply Conditional Access policies to reduce unauthorized access.
  6. Automate joiner, mover, and leaver lifecycle processes.
  7. Ensure employees receive only the access required for their jobs.
  8. Remove old access when employees transfer departments.
  9. Disable accounts and revoke access quickly when users leave the company.
  10. Create approval workflows and access reviews for contractors and sensitive applications.
  11. Identify orphan accounts, dormant accounts, excessive access, and separation-of-duties conflicts.
  13. Protect privileged accounts through least privilege, separate administrator accounts, MFA, emergency-access procedures, and just-in-time access.
  14. Generate reports and audit evidence for security and compliance reviews.

 ## Project Role

For this project, I am acting as the Microsoft Entra ID IAM Engineer responsible for designing, implementing, testing, documenting, and securing the company’s identity environment.

My responsibilities include:

 - Preparing identity data for 50 employees
 - Bulk-provisioning users into Microsoft Entra ID
 - Creating security and dynamic groups
 - Designing an RBAC access model
 - Assigning licenses and application access
 - Configuring authentication methods and MFA
 - Creating Conditional Access policies
 - Building joiner, mover, and leaver processes
 - Implementing Identity Governance controls
 - Designing privileged-access protections
 - Creating PowerShell and Microsoft Graph automation
 - Producing audit reports, runbooks, screenshots, and test results

 ## Expected Business Outcome 
AccessShield Technologies will have a structured and secure cloud identity environment that reduces manual provisioning, limits unnecessary access, improves employee onboarding and offboarding, protects administrator accounts, and produces clear evidence for audits and compliance reviews.

 ## Tools
 -✅ User provisioning
 -✅ RBAC
 -✅ Dynamic groups
 -✅ JML (Joiner–Mover–Leaver)
 -✅ MFA
 -✅ Conditional Access
 -✅ Identity Governance
 -✅ Privileged Access
 -✅ Monitoring
 -✅ Reporting
Use PowerShell, Microsoft Graph, and Azure Automation to reduce repetitive administrative work.
├── 02-Lab-Setup
├── 03-Enterprise-Design
├── 04-Fake-Users
├── 05-Bulk-User-Provisioning
├── 06-Manager-Assignments
├── 07-Security-Groups
├── 08-Dynamic-Groups
├── 09-RBAC
├── 10-Separation-of-Duties
├── 11-License-Management
├── 12-Authentication-MFA
├── 13-Conditional-Access
├── 14-Joiner
├── 15-Mover
├── 16-Leaver
├── 17-Identity-Governance
├── 18-Privileged-Access
├── 19-PowerShell-Automation
├── 20-Microsoft-Graph
├── 21-Monitoring-and-Reporting
└── 22-GitHub-Documentation
