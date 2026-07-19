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
                                                    Chief Executive Officer(CEO)            
                                                                |    
             ┌──────────────────────────────────────┬─────────────────────────────────────────────────────────────────────────────────────────┐
    Chief Information Officer(CIO)         Chief Financial Officer(CFO)                ┬─────────────────────┬─────────────────── Chief Operating Officer(COO)       
             |                                      |                                  |               📈 Sales (10)                          |
         💻 IT (10)                         💰 Finance (8)                                            Sales Manager                ⚙️ Operations (10)
         IAM Manager                         Finance Manager                           |                     │                        Operations Manager
           │    ├── IAM Engineer 1              │   │                                  |      ├── Account Management Lead              │   
           │    ├── IAM Engineer 2              │   ├── Senior Accountant              |      │   ├── Account Manager 1                ├── Operations Team Lead
           │    ├── Identity Analyst            │   ├── Accountant                     |      │   ├── Account Manager 2                │   ├── Operations Coordinator 1
           │    └── Security Analyst            │   ├── Accounts Payable Specialist    |      │   └── Customer Success Manager         │   ├── Operations Coordinator 2
           │                                    │   └── Accounts Receivable Specialist |      |                                        │   ├── Operations Analyst 1
           └── IT Support Manager               │                                      |      └── Senior Sales Representative          │   └── Operations Analyst 2
               ├── Help Desk Technician 1       └── Senior Financial Analyst           |      ├── Sales Representative 1               │
               ├── Help Desk Technician 2              ├── Financial Analyst           |      ├── Sales Representative 2               └── Senior Project Coordinator
               ├── Desktop Support Specialist          └── Budget Analyst              |      ├── Business Development Representative  ├── Logistics Specialist
               └── IT Support Specialist                                               |      └── Sales Coordinator                    ├── Procurement Specialist
                                                                                       │                                               └── Office Administrator                                                                                           👥 HR (8)
                                                                                   HR Manager
                                                                                       │
                                                                                       ├── Senior HR Specialist
                                                                                       │   ├── HR Specialist
                                                                                       │   ├── Benefits Specialist
                                                                                       │   └── Payroll Specialist
                                                                                       │
                                                                                       └── Recruiting Lead
                                                                                       ├── Recruiter 1
                                                                                       ├── Recruiter 2
                                                                                       └── HR Coordinator


 
 
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

 ## 🎯 Project Objectives 
AccessShield Technologies will have a structured and secure cloud identity environment that reduces manual provisioning, limits unnecessary access, improves employee onboarding and offboarding, protects administrator accounts, and produces clear evidence for audits and compliance reviews.

 ## 🛠️ Tools & Technologies
  👥 Microsoft Teams
  📊 Excel / CSV
  ☁️ Microsoft 365
  🔑 Multifactor Authentication (MFA)
  🔒 Conditional Access
  📈 Identity Governance
  🏢 Enterprise Applications
  📝 Visual Studio Code
  💻 PowerShell
  🌐 Microsoft Graph API
  📬 Postman
  📋 Sign-in Logs & Audit Logs

 ## Step 1
  📥 Bulk User Provisionin
  
    Entra ID Admin dashboard→ Users→ Bulk create→ Upload CSV→ Select file→ Submit.
 
    Entra ID Admin dashboard→ Users→ Bulk operation results→ Select operation→ Download results.
 - Created users:
 - Failed users:
 - Duplicate users:
 - Errors:

 ⚡📜PowerShell user creation alternative
  Create:

  Run: 
         
          .\scripts\New-UsersFromCsv.ps1 `
    -CsvPath "C:\Private\AccessShieldUsers.csv" `
    -WhatIf

 Completion
 ✅Downloaded Microsoft’s template
 ✅Prepared 50 fake users
 ✅Uploaded users
 ✅Corrected failures
 ✅Saved the result report
 
 ## Step 2 
  👔 Manager Assignments
       
    Users→ All users→ Select employee→ Properties→ Manager→ Edit→ Search manager→ Select→ Save
Use your spreadsheet manager column

    ManagerUPN
Connect to Microsoft Graph
Create:

    scripts/Connect-MicrosoftGraph.ps1
Assign managers with PowerShell

Find users without managers

 ✅Assigned one manager manually
 ✅Connected to Graph
 ✅Assigned managers from CSV
 ✅Reviewed missing managers
   
  ## Step 3
  👨‍👩‍👧‍👦 Security Groups

    Entra ID→ Groups→ All groups→ New group 
    Group type → Security
    Membership type → Assigned

Create:

    SG-Department-Executives
    SG-Department-IT
    SG-Department-HR
    SG-Department-Finance
    SG-Department-Sales
    SG-Department-Operations

Application groups
Create:

    SG-App-Finance
    SG-App-HR
    SG-App-Sales
    SG-App-Operations
    SG-App-Helpdesk
    SG-App-VPN
  
Security-Control Groups
Create:

    SG-CA-MFA-Pilot
    SG-CA-Privileged-Users
    SG-AccessReview-Contractors
    SG-Leavers

PowerShell

Add a user manually

    Groups→ Select group→ Members→ Add members→ Search user→ Select 

PowerShell 

 ✅Created department groups
 ✅Created application groups
 ✅Created control groups
 ✅Added members

  ## Step 4
  ⚡ Dynamic Groups

    Groups→ All groups→ New group

    Group type → Security
    Membership type → Dynamic User
    Group name → DYN-Department-IT

  Dynamic Query

    Property → department
    Operator → Equals
    Value → Information Technology
  Rule:

    (user.department -eq "Information Technology") 
 
  Remaining Department Groups
  Create:

    DYN-Department-HR
    DYN-Department-Finance
    DYN-Department-Sales
    DYN-Department-Operations
  Rules:

    (user.department -eq "Human Resources")
    (user.department -eq "Finance")
    (user.department -eq "Sales")
    (user.department -eq "Operations")
  Contractor Group
  Create:

    DYN-Contractors
 Rule:

    (user.employeeType -eq "Contractor")

 Test a dynamic group   

    Users→ Select user→ Properties→ Department→ Edit
 Change:
      
    Sales
 to:

    Information Technology
 Verify:

    User removed from DYN-Department-Sales
    User added to DYN-Department-IT
  ✅Created five department dynamic groups
  ✅Created contractor dynamic group
  ✅Tested automatic membership
  ✅Captured before-and-after evidence
    
  ## Step 5
  🔑 Role-Based Access Control (RBAC)

  Create the RBAC spreadsheet

    JobTitle
    Department
    DepartmentGroup
    ApplicationGroup
    License
    AdministrativeRole
    ApprovalRequired
  Assign department access

    Finance workers → SG-Department-Finance
    HR workers → SG-Department-HR
    Sales workers → SG-Department-Sales

  Assign application access

    Financial roles → SG-App-Finance
    HR roles → SG-App-HR
    Sales roles → SG-App-Sales
    Help Desk roles → SG-App-Helpdesk
 Find users outside the model
 
 Powershell

  ✅Created RBAC matrix
  ✅Assigned department access
  ✅Assigned application access
  ✅Documented exceptions

  ## Step 6
  ⚖️ Separation of Duties (SoD)

  Create Finance conflict groups
  Create:

    SG-Finance-Payment-Creator
    SG-Finance-Payment-Approver

  HR conflict groups   
  Create:

    SG-HR-Record-Editor
    SG-HR-Record-Auditor
  
  To Simulate a conflict i well add one fake Finance user to both:

    SG-Finance-Payment-Creator
    SG-Finance-Payment-Approver
  
  Find SoD conflicts with PowerShell
  
  Powershell

 Remediate 
 Remove one group membership:

 Powershell

 ✅Created SoD groups
 ✅Created a test conflict
 ✅Detected the conflict
 ✅Removed conflicting access
 ✅Documented remediation
  
  ## Step 7
  🎫 License Management

  Review licenses

    Billing→ Licenses→ All products
  Record:

    Product
    Total
    Assigned
    Available

  Check usage location

    Users→ Select user→ Properties→ Usage location→ United States→ Save
  Assign a license manually

  Users→ Select user→ Licenses→ Assignments→ Select product→ Save

  Export licenses

  PowerShell

  ✅Reviewed license inventory
  ✅Updated usage locations
  ✅Assigned pilot licenses
  ✅Exported license report
  
  ## Step 8
  🔐 Authentication & MFA

  Add pilot 5 users

    SG-CA-MFA-Pilot

  Enable Microsoft Authenticator

    Authentication methods→ Policies→ Microsoft Authenticator→ Enable→ Target selected groups→ SG-CA-MFA-Pilot→ Save

   Enable Temporary Access Pass

    Authentication methods→ Policies→ Temporary Access Pass→ Enable→ Add SG-CA-MFA-Pilot 
  Settings:

    Lifetime → 60 minutes
    One-time use → Yes
 
  Create one TAP Do not.

  Users→ Select pilot user→ Authentication methods→ Add authentication method→ Temporary Access Pass→ Add 

  Test registration
  
  ✅Created MFA pilot
  ✅Enabled Authenticator
  ✅Enabled TAP
  ✅Tested one user
  ✅ Hid all authentication secrets
  ## Step 9
  🛡️ Conditional Access

    Conditional Access→ Policies→ New policy
  Name

    CA001-Require-MFA-Pilot
  Configure:

    Users → SG-CA-MFA-Pilot
    Target resources → All resources
    Grant → Require multifactor authentication
    State → Report-only
  What If

    Conditional Access→ What If→ Select user→ Select resource→ Run

  Create legacy authentication policy
  Name:

    Users → Pilot group
    Target resources → All resources
    Conditions → Client apps
    Select → Legacy authentication clients
    Grant → Block access
    State → Report-only

 Create administrator MFA policy
 Name:

    CA003-Require-MFA-Administrators
    
 Configure:

    Users → Directory roles
    Select administrator roles
    Target resources → All resources
    Grant → Require MFA
    State → Report-only 
  
Create phishing-resistant admin policy
Name:

    CA004-Phishing-Resistant-MFA-Privileged

  Configure:

    Users → Selected privileged roles
    Grant → Require authentication strength
    Authentication strength → Phishing-resistant MFA
    State → Report-only
  ✅Created MFA policy
  ✅Used Report-only mode
  ✅Used What If
  ✅Created legacy-authentication policy
  ✅Created administrator policies  
  
  ## Step 10
  🚀 Joiner Process
  Create:

    Jordan Testjoiner
    Junior Financial Analyst
    Finance
    Employee
    US
 
    Users→ New user→ Create new user
  Assign manager  

    Jordan→ Properties→ Manager→ Finance Manager→ Save
  Assign access

    SG-Department-Finance
    SG-App-Finance
    SG-CA-MFA-Pilot
  Assign license

    Jordan→ Licenses→ Assignments→ Select available license→ Save
  Validate joiner with PowerShell

  PowerShell

  ✅Created Jordan
  ✅Assigned manager
  ✅Assigned groups
  ✅Assigned license
  ✅Added TAP
  ✅Validated onboarding
  
  ## Step 11
  🔄 Mover Process

  Sales user
  Record:

    Current department
    Current title
    Current manager
    Current groups
    Current license
   Update attributes

  PowerShell

  Assign new manager

  PowerShell

  Remove Sales groups

  PowerShell

  Add Finance groups

  PowerShell

  Check privilege creep

    Sales department access
    Sales application access
    Old manager relationship
    Unapproved direct assignments
  ✅Recorded old access
  ✅Updated department and title
  ✅Updated manager
  ✅Removed Sales access
  ✅Added Finance access
  ✅Verified privilege-creep removal
 
  ## Step 12
  🚪 Leaver Process

  Inventory the user
  Record:

    Groups
    Licenses
    Applications
    Authentication methods
    Admin roles
    Account status
  Disable account
  
  Powershell

  Revoke sessions

  Powershell

  Remove group memberships

  powerShell

  Remove licenses

  PowerShell

  Add to leaver tracking group

  PowerShell

  Ensure SG-Leavers grants no access.
  
  ✅Inventoried account
  ✅Disabled account
  ✅Revoked sessions
  ✅Removed groups
  ✅Removed licenses
  ✅Removed privileged access
  ✅Added to tracking group
  
  ## Step 13
  🏛️ Identity Governance

  Create contractor review group

    SG-AccessReview-Contractors
  Add all contractors.

  Create access review

    Identity Governance→ Access reviews→ New access review
    Teams and groups
    Select SG-AccessReview-Contractors
  Configure:

    Reviewer → Group owner or selected manager
    Duration → 7 days
    Frequency → Monthly

  Test review decisions
  Approve one contractor.

  Deny one contractor.

  Apply results.

  Find orphan accounts
    
    Active account with no manager
    Contractor with no sponsor
    Service account with no owner
    Disabled user with active license

  PowerShell

  Create audit script

  PowerShell

  ✅Created contractor review
  ✅Approved and denied test access
  ✅Generated orphan-account report
  ✅Generated contractor report
  ✅Documented remediation

  ## Step 14
  👑 Privileged Access

  Create separate admin account

    Normal:
    maya.collins@yourtenant.onmicrosoft.com
    Admin:
    adm-maya.collins@yourtenant.onmicrosoft.com

  Create privileged groups

    SG-Privileged-Helpdesk
    SG-Privileged-Identity-Admins
    SG-Privileged-Security-Admins
    SG-Privileged-Global-Admins

  Map least-privileged roles

    Help Desk Technician→ Helpdesk Administrator
    MFA Support→ Authentication Administrator
    Identity Administrator→ User Administrator
    Group Administrator→ Groups Administrator
    Security Analyst → Security Reader

  Create emergency access accounts

    Emergency use only
    Credentials stored securely
    Sign-in alerts enabled
    Quarterly testing
    Post-use review required
  
  Configure PIM

    Identity Governance→ Privileged Identity Management→ Microsoft Entra roles→ Assignments→ Add assignments
  Select:

    Assignment type → Eligible
    Duration → Time-limited

  Configure activation:

    Require MFA
    Require justification
    Require approval
    Maximum duration → 1 hour

  Export active privileged roles

  PowerShell

  ✅Created separate admin identity
  ✅Created privileged groups
  ✅Applied least privilege
  ✅Created emergency accounts
  ✅Configured or simulated PIM/JIT
  ✅Exported privileged roles
  
  ## Step 15
  💻 PowerShell Automation

    Create script folders
    scripts/
    ├── provisioning/
    ├── groups/
    ├── lifecycle/
    ├── governance/
    ├── privileged-access/
    └── reporting/
  Add core scripts

    Connect-MicrosoftGraph.ps1
    New-UsersFromCsv.ps1
    Set-ManagersFromCsv.ps1
    New-SecurityGroups.ps1
    Add-DepartmentGroupMembers.ps1
    Invoke-Joiner.ps1
    Invoke-Mover.ps1
    Invoke-Leaver.ps1
    Export-IAMAuditReports.ps1
    Export-PrivilegedRoles.ps1
  Add error handling

  PowerShell

  Add WhatIf support
  use:

  PoweShell

  Then:

  Powershell

  Do not hard-code secrets

  PowerShell

  ✅Organized script folders
  ✅Added core scripts
  ✅Added error handling
  ✅Added -WhatIf
  ✅Removed hard-coded secrets
 
  ## Step 16
  🌐 Microsoft Graph API

  
  Review the Graph endpoint format

    https://graph.microsoft.com/v1.0/
    GET /users
    GET /groups
    POST /users
    PATCH /users/{id}
  Get users through PowerShell SDK

  PowerShell

  Use Invoke-MgGraphRequest 

  PowerShell

  Create a user with REST-style Graph

  PowerShell

  Update a user
  
  PowerShell
  
  Save JSON examples

    20-Microsoft-Graph-API/
    ├── get-users.json
    ├── create-user.json
    ├── update-user.json
    ├── add-group-member.json
    └── README.md
  ✅Used Graph SDK
  ✅Used Invoke-MgGraphRequest
  ✅Created a test user
  ✅Updated a test user
  ✅Saved sanitized JSON examples
 
  ## Step 17
  📊 Monitoring & Reporting
  
  Review sign-in logs

    Monitoring & health→ Sign-in logs
  Review:

    User
    Application
    IP address
    Location
    Status
    Authentication requirement
    Conditional Access
    Failure reason
  Filter a pilot user

    Sign-in logs→ Add filters→ User→ Select pilot user
  Review audit logs

    Monitoring & health→ Audit logs
  Search:
   
    Add user
    Update user
    Add group member
    Remove group member
    Update Conditional Access policy
    Assign role
  Export users

  PowerShell

 Export groups

 PowerShell

 Create the final evidence folders
 
21-Monitoring-and-Reporting/
├── screenshots/
│   ├── sign-in-success.png
│   ├── sign-in-failure.png
│   ├── conditional-access-result.png
│   └── audit-log-change.png
├── reports/
│   ├── AllUsers.csv
│   ├── AllGroups.csv
│   ├── LicenseReport.csv
│   ├── UsersWithoutManagers.csv
│   ├── ContractorInventory.csv
│   ├── DisabledUsersWithLicenses.csv
│   ├── SoDConflicts.csv
│   └── PrivilegedRoleAssignments.csv
└── README.md
Write findings

    Finding:
    One disabled contractor retained a Microsoft 365 license.
    Risk:
    The organization continued paying for an unused license.
    Remediation:
    The license was removed and the leaver checklist was updated.
  ✅Reviewed sign-in logs
  ✅Reviewed Conditional Access results
  ✅Reviewed audit logs
  ✅Exported user and group reports
  ✅Documented findings
  ✅Added safe GitHub evidence




  
└── 22-GitHub-Documentation
