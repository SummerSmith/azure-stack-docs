---
author: sethmanheim
ms.author: sethm
ms.service: azure-stack
ms.topic: include
ms.date: 05/02/2022
ms.reviewer: abha
ms.lastreviewed: 05/02/2022

---

If you have not installed the AksHci PowerShell module, run the following commands to install the modules.

> [!IMPORTANT]  
> You must close all existing PowerShell windows and open a fresh administrative session to install the pre-requisite PowerShell packages and modules. 

```powershell
Install-Module -Name Az.Accounts -Repository PSGallery -RequiredVersion 2.2.4
Install-Module -Name Az.Resources -Repository PSGallery -RequiredVersion 3.2.0
Install-Module -Name AzureAD -Repository PSGallery -RequiredVersion 2.0.2.128
Install-Module -Name AksHci -Repository PSGallery
```

```powershell
Import-Module Az.Accounts
Import-Module Az.Resources
Import-Module AzureAD
Import-Module AksHci
```
**If you are using remote PowerShell, you must use CredSSP.** 

> [!IMPORTANT]  
> **You must close all existing PowerShell windows** again to ensure that loaded modules are refreshed. Please do not continue to the next step until you have closed all PowerShell windows.

**Validate your installation.**

> [!IMPORTANT]  
> **Close all PowerShell windows** and reopen a new administrative session to check if you have the latest version of the PowerShell module.

```powershell
Get-Command -Module AksHci
```

To view the complete list of AksHci PowerShell commands, see [AksHci PowerShell](../reference/ps/index.md).
