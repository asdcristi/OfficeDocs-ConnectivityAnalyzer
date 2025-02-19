---
title: Exchange ActiveSync Returned an HTTP 451 Error
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Microsoft Remote Connectivity Analyzer tool returns the following error: "Exchange ActiveSync returned an HTTP 451 response. (Device Misconfigured)."'
ms.date: 05/08/2020
---

# Exchange ActiveSync Returned an HTTP 451 Error

_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer sends an Exchange ActiveSync FolderSync command to the URL specified. If an HTTP 451 response code is received from the server, then the Microsoft Remote Connectivity Analyzer tool returns the following error.

"Exchange ActiveSync returned an HTTP 451 response. (Device Misconfigured)."

<div>

## For More Information

Exchange 2007 returns an HTTP 451 response to an Exchange ActiveSync client when it determines that the device should be using a "better" Client Access server for ActiveSync connectivity. The logic used to determine if a Client Access server is "better" for a device to be using is based on Active Directory sites and whether a Client Access server is considered "Internet-facing." If the ExternalUrl property on the Microsoft-Server-ActiveSync virtual directory is specified, then that Client Access server is considered to be "Internet-Facing" for Microsoft ActiveSync connectivity.

If the user mailbox being tested is not in the same Active Directory site as the Client Access server that is being accessed, there may be a Client Access server in the site with the mailbox server that has the ExternalUrl property set. If you are attempting to configure ActiveSync to proxy from an Internet-facing site to a second site (Intranet), ensure that the ExternalUrl property is not set on the Microsoft-Server-ActiveSync virtual directory in the Intranet site.

For more information about configuring Client Access servers for Proxy and Redirection, see [Understanding Proxying and Redirection](https://go.microsoft.com/fwlink/?linkid=105411).

If you have multiple Client Access servers in the same Active Directory site as the Client Access servers being tested, ensure that the ExternalUrl parameter is populated on each of the Microsoft-Server-ActiveSync virtual directories. If the ExternalUrl property is missing on the Client Access server being tested, then this error can occur.

For more information about setting the ExternalUrl attribute on the ActiveSync virtual directory, see [Set-ActiveSyncVirtualDirectory](https://go.microsoft.com/fwlink/?linkid=161796).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

