---
title: Protect derived domain credentials with Credential Guard (Windows 10)
description: Introduced in Windows 10 Enterprise, Credential Guard uses virtualization-based security to isolate secrets so that only privileged system software can access them.
ms.assetid: 4F1FE390-A166-4A24-8530-EA3369FEB4B1
ms.prod: w10
ms.mktglfcycl: explore
ms.sitesec: library
ms.pagetype: security
localizationpriority: high
author: brianlic-msft
---

# Protect derived domain credentials with Credential Guard

**Applies to**
-   Windows 10
-   Windows Server 2016

Prefer video? See [Credential Theft and Lateral Traversal](https://mva.microsoft.com/en-us/training-courses/deep-dive-into-credential-guard-16651?l=cfGBPlIyC_9404300474)  in the Deep Dive into Credential Guard video series.

Introduced in Windows 10 Enterprise and Windows Server 2016, Credential Guard uses virtualization-based security to isolate secrets so that only privileged system software can access them. Unauthorized access to these secrets can lead to credential theft attacks, such as Pass-the-Hash or Pass-The-Ticket. Credential Guard prevents these attacks by protecting NTLM password hashes, Kerberos Ticket Granting Tickets, and credentials stored by applications as domain credentials.

By enabling Credential Guard, the following features and solutions are provided:

-   **Hardware security** NTLM, Kerberos, and Credential Manager take advantage of platform security features, including Secure Boot and virtualization, to protect credentials.
-   **Virtualization-based security** Windows NTLM and Kerberos derived credentials and other secrets run in a protected environment that is isolated from the running operating system.
-   **Better protection against advanced persistent threats** When Credential Manager domain credentials, NTLM, and Kerberos derived credentials are protected using virtualization-based security, the credential theft attack techniques and tools used in many targeted attacks are blocked. Malware running in the operating system with administrative privileges cannot extract secrets that are protected by virtualization-based security. While Credential Guard is a powerful mitigation, persistent threat attacks will likely shift to new attack techniques and you should also incorporate Device Guard and other security strategies and architectures.

 
## Related topics

- [Isolated User Mode in Windows 10 with Dave Probert (Channel 9)](https://channel9.msdn.com/Blogs/Seth-Juarez/Isolated-User-Mode-in-Windows-10-with-Dave-Probert)
- [Isolated User Mode Processes and Features in Windows 10 with Logan Gabriel (Channel 9)](http://channel9.msdn.com/Blogs/Seth-Juarez/Isolated-User-Mode-Processes-and-Features-in-Windows-10-with-Logan-Gabriel)
- [More on Processes and Features in Windows 10 Isolated User Mode with Dave Probert (Channel 9)](https://channel9.msdn.com/Blogs/Seth-Juarez/More-on-Processes-and-Features-in-Windows-10-Isolated-User-Mode-with-Dave-Probert)
- [Mitigating Credential Theft using the Windows 10 Isolated User Mode (Channel 9)](https://channel9.msdn.com/Blogs/Seth-Juarez/Mitigating-Credential-Theft-using-the-Windows-10-Isolated-User-Mode)
- [Protecting network passwords with Windows 10 Credential Guard](https://www.microsoft.com/itshowcase/Article/Content/831/Protecting-network-passwords-with-Windows-10-Credential-Guard)
- [Enabling Strict KDC Validation in Windows Kerberos](http://www.microsoft.com/download/details.aspx?id=6382)
- [What's New in Kerberos Authentication for Windows Server 2012](http://technet.microsoft.com/library/hh831747.aspx)
- [Authentication Mechanism Assurance for AD DS in Windows Server 2008 R2 Step-by-Step Guide](http://technet.microsoft.com/library/dd378897.aspx)
- [Trusted Platform Module](trusted-platform-module-overview.md)
 

## See also

**Deep Dive into Credential Guard: Related videos**

[Credentials protected by Credential Guard](https://mva.microsoft.com/en-us/training-courses/deep-dive-into-credential-guard-16651?l=pdc37LJyC_1204300474)