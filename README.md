# IAM

## Microsoft Entra ID – MFA & Conditional Access Security Implementation

### Overview

This project demonstrates the implementation of enterprise identity security controls within Microsoft Entra ID using Multifactor Authentication (MFA), Conditional Access policies, role-based access management, and organizational security groups.

The lab simulates a real-world Identity and Access Management (IAM) environment where privileged accounts and organizational users are secured through authentication policies and administrative access controls.

---

### Technologies Used

- Microsoft Entra ID
- Conditional Access Policies
- Microsoft Authenticator
- Microsoft 365 Developer Tenant
- Administrative Roles
- Security Groups
- MFA Authentication Workflows

---

### Objectives

- Create enterprise users and organizational groups
- Assign privileged administrative roles
- Implement Multifactor Authentication (MFA)
- Configure Conditional Access policies
- Enforce secure authentication controls
- Simulate enterprise RBAC workflows
- Protect privileged administrative accounts

---

### Environment Setup

#### Microsoft Entra Tenant Configuration

The lab environment was configured within a Microsoft 365 Developer Tenant using Microsoft Entra ID.

##### Security Defaults Enabled

Security defaults were initially enabled to provide baseline identity protection controls.

![Tenant Security Defaults Enabled](screenshots/security-defaults-enabled.png)

##### Security Defaults Disabled for Conditional Access Testing

Security defaults were later disabled to allow custom Conditional Access policies to be implemented and tested.

![Security Defaults Disabled](screenshots/security-defaults-disabled.png)

---

### User Provisioning

Organizational users were provisioned to simulate different enterprise departments and administrative roles.

| User | Role |
|------|------|
| HR User | Department User |
| Finance User | Department User |
| IT Admin | Privileged Administrator |

#### HR User Provisioning

The HR user account was created within Microsoft Entra ID.

![HR User Creation](screenshots/hr-user-creation.png)

#### Finance User Provisioning

The Finance user account was provisioned with organizational identity settings.

![Finance User Creation](screenshots/finance-user-creation.png)

#### IT Administrator Provisioning

An IT Administrator account was created to simulate privileged administrative access.

![IT Admin Account Creation](screenshots/it-admin-creation.png)

#### Organizational Users Overview

The tenant user directory displayed all organizational users created during the lab.

![Organizational Users List](screenshots/users-overview.png)

---

### Security Group Administration

Security groups were created to simulate group-based access management and enterprise RBAC structures.

#### HR Security Group

An HR-Team security group was created for departmental access management.

![HR-Team Security Group Creation](screenshots/hr-security-group.png)

#### Finance Security Group

A Finance-Team security group was created for identity segmentation and departmental resource access.

![Finance-Team Security Group Creation](screenshots/finance-security-group.png)

#### IT Security Group

An IT-Team security group was created to manage administrative users and privileged access assignments.

![IT-Team Security Group Overview](screenshots/it-security-group.png)

#### Security Groups Overview

All organizational security groups were successfully created within Microsoft Entra ID.

![Security Groups Overview](screenshots/security-groups-overview.png)

---

### Administrative Role Assignment

Role-Based Access Control (RBAC) was implemented by assigning administrative privileges to the IT Admin account.

**Role Assigned:** `User Administrator`

**Actions Performed:**
1. Navigated to Roles and Administrators
2. Selected the User Administrator role
3. Assigned privileged administrative access to IT Admin

![User Administrator Role Assignment](screenshots/role-assignment.png)

---

### Conditional Access Policy Configuration

Conditional Access policies were implemented to require MFA for administrative and organizational users.

#### Policy 1 – Administrative Users

**Policy Name:** `CA-Require-MFA-Admins`

This policy targeted privileged administrative users to enforce MFA during sign-in attempts.

**Actions Performed:**
1. Selected directory roles
2. Targeted User Administrator role
3. Configured policy enforcement settings

![Conditional Access Policy for Admin Users](screenshots/ca-policy-admins.png)

#### Grant Controls Configuration

Grant controls were configured to require MFA authentication before administrative access was granted.

**Actions Performed:**
1. Enabled "Require Multifactor Authentication"
2. Configured access enforcement controls
3. Required all selected controls

![MFA Grant Control Configuration](screenshots/ca-grant-controls.png)

#### Policy 2 – All Users

**Policy Name:** `CA-Require-MFA-All-Users`

A second Conditional Access policy was created to enforce MFA across all organizational users.

**Actions Performed:**
1. Targeted all users
2. Configured MFA enforcement
3. Applied organization-wide authentication protections

![Conditional Access Policy for All Users](screenshots/ca-policy-all-users.png)

---

### MFA Registration Workflow

Users completed MFA enrollment using Microsoft Authenticator.

#### Microsoft Authenticator Enrollment

The authentication application was configured for secure MFA sign-in approval.

![Microsoft Authenticator Enrollment](screenshots/authenticator-enrollment.png)

#### MFA Challenge Verification

Users completed MFA verification using number matching authentication.

![MFA Number Matching Challenge](screenshots/mfa-number-matching.png)

#### Authenticator Registration Completed

The MFA setup process was successfully completed.

![Authenticator Successfully Added](screenshots/authenticator-complete.png)

---

### Authentication Workflow Testing

Authentication workflows were tested to validate Conditional Access and MFA enforcement.

#### Password Update and Secure Sign-In

Users completed secure password initialization before authentication.

![Initial Password Update Workflow](screenshots/password-update.png)

#### Azure Portal Access Verification

Successful sign-in confirmed Conditional Access and MFA enforcement functionality.

![Successful Azure Portal Authentication](screenshots/azure-portal-access.png)

---

### Security Concepts Demonstrated

| Concept | Description |
|--------|-------------|
| Identity and Access Management (IAM) | Lifecycle management of users and access |
| Multifactor Authentication (MFA) | Additional authentication factor enforcement |
| Conditional Access Policies | Context-aware access control rules |
| Role-Based Access Control (RBAC) | Privilege assignment based on roles |
| Identity Governance | Structured user and group management |
| User Provisioning | Creating and managing enterprise identities |
| Group-Based Access Management | Departmental access segmentation |
| Privileged Access Management (PAM) | Protecting high-privilege accounts |
| Authentication Security | Secure sign-in workflow enforcement |

---

### Key Takeaways

This project demonstrated how Microsoft Entra ID can be used to strengthen enterprise authentication security through:

- **Conditional Access policies** to enforce authentication requirements based on user role and context
- **Multifactor Authentication** to mitigate credential compromise risks
- **Role assignments** to delegate administrative responsibilities using RBAC principles
- **Security group administration** to manage identity segmentation across departments
- **Privileged account protection** for IT Administrator accounts with elevated access

---

### Conclusion

This project successfully implemented enterprise IAM security controls using Microsoft Entra ID. Through Conditional Access policies, MFA enforcement, role assignments, and security group administration, the environment achieved stronger identity protection and secure authentication management.

The project provided hands-on experience with enterprise IAM concepts including RBAC, MFA, identity governance, administrative role delegation, and authentication security enforcement.
