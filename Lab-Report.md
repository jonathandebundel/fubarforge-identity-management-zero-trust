\# FubarForge Identity Management Lab Report



This document provides a technical overview of the hybrid identity lab environment and the security controls implemented within the FubarForge project.



---



\# Environment Overview



The lab simulates a hybrid enterprise identity infrastructure where an on-premises Active Directory environment is integrated with Microsoft Entra ID.



Core infrastructure components include:



\- Windows Server 2025 Domain Controller

\- Microsoft Entra Connect

\- Microsoft Entra ID tenant

\- Microsoft Intune device management

\- Conditional Access policies

\- Privileged Identity Management



The objective is to implement a Zero Trust identity architecture.



---



\# Active Directory



The on-premises environment includes:



\- Organizational Units

\- Security groups

\- User accounts

\- Domain controller services



Active Directory acts as the authoritative identity source for the environment.



Users and groups are synchronized to Microsoft Entra ID using Microsoft Entra Connect.



---



\# Hybrid Identity



Microsoft Entra Connect synchronizes selected organizational units to the cloud directory.



Configuration includes:



\- OU filtering

\- Password hash synchronization

\- Hybrid identity support



This allows users to authenticate using the same identity both on-premises and in cloud services.



---



\# Conditional Access



Conditional Access policies enforce security requirements for authentication.



Policies implemented include:



\- MFA required for users

\- MFA required for privileged accounts

\- Blocking legacy authentication

\- Responding to risky sign-ins

\- Password reset for compromised accounts

\- Requiring compliant devices for access



These policies implement a Zero Trust access model.



---



\# Privileged Identity Management



Privileged roles are protected using Microsoft Entra Privileged Identity Management.



Key protections include:



\- Just-in-time role activation

\- Activation requiring justification

\- Temporary role assignment

\- Role activation logging



This reduces persistent privileged access.



---



\# Device Compliance



Microsoft Intune is used to manage device compliance.



Two device types are demonstrated:



\- Hybrid joined Windows device

\- Cloud joined Windows device



Conditional Access policies require devices to be compliant before access to cloud resources is granted.



---



\# Security Monitoring



Authentication activity is monitored through:



\- Sign-in logs

\- Conditional Access logs

\- Privileged Identity Management audit logs



These logs provide visibility into authentication events and security policy enforcement.



---



\# Security Testing



Security controls were validated through simulated attack scenarios using Kali Linux.



Test scenarios included:



\- Authentication attempts from unmanaged devices

\- Failed authentication attempts

\- Conditional Access blocking unauthorized access



The results demonstrate that the implemented security controls effectively prevent unauthorized access.



---



\# Conclusion



The FubarForge lab demonstrates how hybrid identity infrastructures can implement a Zero Trust security model using Microsoft Entra ID, Conditional Access, and device compliance controls.



The environment illustrates how identity security, privileged access protection, and authentication monitoring work together to protect enterprise systems.

