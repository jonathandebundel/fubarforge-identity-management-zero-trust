\# Security Control Validation



This section demonstrates how security controls implemented in the FubarForge identity lab respond to unauthorized or non-compliant access attempts.



The tests simulate realistic authentication scenarios including unmanaged devices, failed login attempts, and Conditional Access enforcement.



\## Test Scenarios



\### Unmanaged Device Access Attempt

Authentication attempt from a Linux system (Kali) without device compliance.



Result:

Conditional Access blocked authentication because the device did not meet Microsoft Intune compliance requirements.



\### Conditional Access Enforcement

Access to Microsoft cloud resources requires:



\- MFA authentication

\- Intune compliant device

\- Entra managed identity



Non-compliant devices are denied access.



\### MFA Enforcement

Sign-in attempts require multi-factor authentication for both users and administrators.



Sign-in logs confirm MFA challenge events.



\### Authentication Monitoring

Failed login attempts are visible in Microsoft Entra sign-in logs, demonstrating monitoring and detection capabilities.



\## Security Model



This lab implements a Zero Trust approach:



Identity verification  

\+  

Device compliance  

\+  

Conditional Access enforcement



Access is only granted when all conditions are satisfied.

