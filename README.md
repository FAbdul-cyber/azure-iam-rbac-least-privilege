
# Azure Identity and Access Management (IAM) Lab

## Project Overview
This hands-on project demonstrates how I configured identity and access management in Microsoft Azure using Microsoft Entra ID and Azure Role-Based Access Control (RBAC).

The scenario involved provisioning three employees from Development, Human Resources, and Security and assigning permissions based on their job responsibilities.

## Project Objectives
- Create three user accounts in Microsoft Entra ID.
- Assign appropriate built-in Azure RBAC roles.
- Restrict access to a specific Azure resource group.
- Apply the principle of least privilege.
- Verify the assigned permissions.

## Tools and Technologies
- Microsoft Azure Portal
- Microsoft Entra ID
- Azure Role-Based Access Control (RBAC)
- Azure Resource Groups

## Implementation

### 1. User Provisioning
Created three user accounts in Microsoft Entra ID representing employees from Development, HR, and Security.

### 2. Role Assignments

| User | Department | Azure RBAC Role | Purpose |
|---|---|---|---|
| Fahima Abdul | Development | Contributor | Create, modify, and delete Azure resources without managing RBAC role assignments |
| Jennifer Halvey | HR | Reader | View Azure resource information without modifying resources |
| Kattie Hoven | Security | Security Reader | View supported security alerts, recommendations, and security information |

### 3. Scope Configuration
Assigned the roles at the Cyberproject1 resource group scope rather than the subscription scope to limit access to the lab environment.

### 4. Verification
Verified all three role assignments under Cyberproject1 > Access control (IAM) > Role assignments.

## Security Principles Applied

### Principle of Least Privilege
Each user received permissions appropriate to their responsibilities, with access limited to the Cyberproject1 resource group.

### Role-Based Access Control
Used built-in Azure roles to separate development, read-only, and security-monitoring responsibilities.

## Results
Successfully created three Microsoft Entra ID users and verified their Azure RBAC role assignments at the resource group level.

## Security Considerations
- Contributor can delete resources within the assigned scope but cannot assign Azure RBAC roles.
- Reader does not automatically provide access to all application data or logs.
- Security Reader visibility depends on the supported security services and assigned scope.
- Role assignment verification does not replace testing each user's effective access.

## Evidence
![Azure RBAC role assignments](Screenshot%202026-11-01%20142951.png)
## Lessons Learned
This lab strengthened my understanding of user provisioning, Azure RBAC, permission scopes, and the importance of reviewing access assignments before applying them.
