<h2>🏢Enterprise-EntraID-Project

  ## Business-Scenario
AccessShield Technologies is a growing technology and consulting company with employees in New York, New Jersey, Atlanta and remote locations.

The company recently hired 50 workers across:
- Executive Leadership
- Information Technology
- Human Resources
- Finance
- Sales
- Operations

Manual processes will create several business and security problems:

 - New employees sometimes wait too long to receive system access.
 - Users may receive access that does not match their job responsibilities.
 - Employees who transfer departments may keep access from their previous roles.
 - Contractors may remain active after their contracts expire.
 - Administrator accounts may have more privileges than necessary.
 - Managers have limited visibility into who has access to company applications.
 - Audit evidence is difficult to collect.
 - User onboarding and offboarding require too much manual work.

The leadership team has asked the Identity and Access Management team to design and implement a secure Microsoft Entra ID environment.

 ## Department Structure
 <img width="494" height="162" alt="Dapartment Structure" src="https://github.com/user-attachments/assets/3635c61d-74db-4488-b3bf-aea1b8007788" />


      
                      👔 Executive Leadership (4)
                                   │
          ┌───────────────┬───────────────┬───────────────┐
          │               │               │
       💻 IT (10)     💰 Finance (8)   ⚙️ Operations (10)
         │               │               │
         │               │               │
     👥 HR (8)         📈 Sales (10)

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
  ✅ User provisioning
  ✅ RBAC
  ✅ Dynamic groups
  ✅ JML (Joiner–Mover–Leaver)
  ✅ Multi-Factor Authentication (MFA)
  ✅ Conditional Access
  ✅ Identity Governance
  ✅ Enterprise Applications
  ✅ Monitoring
  ✅ Reporting
  ✅ PowerShell
  ✅ Microsoft Graph
 ## Step 1
  📥 Bulk User Provisionin
  
 Entra ID Admin dashboard→ Users→ Bulk create→ Upload CSV→ Select file→ Submit.
 
 Entra ID Admin dashboard→ Users→ Bulk operation results→ Select operation→ Download results.
 - Created users:
 - Failed users:
 - Duplicate users:
 - Errors:

       ⚡📜PowerShell user creation alternative
        

    
    
                          
                                                                      
                    
      
    
 ## Step 2 
  👔 Manager Assignments
  ## Step 3
  👨‍👩‍👧‍👦 Security Groups
  ## Step 4
  ⚡ Dynamic Groups
  ## Step 5
  🔑 Role-Based Access Control (RBAC)
  ## Step 6
  ⚖️ Separation of Duties (SoD)
  ## Step 7
  🎫 License Management
  ## Step 8
  🔐 Authentication & MFA
  ## Step 9
  🛡️ Conditional Access
  ## Step 10
  🚀 Joiner Process
  ## Step 11
  🔄 Mover Process
  ## Step 12
  🚪 Leaver Process
  ## Step 13
  🏛️ Identity Governance
  ## Step 14
  👑 Privileged Access
  ## Step 15
  💻 PowerShell Automation
  ## Step 16
  🌐 Microsoft Graph API
  ## Step 17
  📊 Monitoring & Reporting
  
  




  
└── 22-GitHub-Documentation
