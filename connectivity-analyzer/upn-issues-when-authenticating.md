---
title: UPN issues when authenticating
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: UPN issues when authenticating
ms.date: 05/08/2020
---

# UPN issues when authenticating


_**Topic Last Modified:** 2012-02-24_

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to simulate the authentication process that a client uses to authenticate by using identity federation. Occasionally, users experience an issue that is commonly indicated by an Outlook client continuously prompting them for credentials.

<div id="sectionSection0" class="section">

Many different issues can cause an Outlook client to repeatedly prompt for authentication. For example, this symptom can occur when a federated user uses a UPN that does not reference a federated domain.

The Remote Connectivity Analyzer displays a warning message when the authentication fails. However, this message can sometimes be generic and not specify the cause of the failure. In these cases, many different possible solutions may exist. However, all solutions to these issues are related to the on-premise ADFS configuration.

<div>

## More information

For more information about how to troubleshoot this issue, [A federated user is prompted for credentials or cannot sign in to Microsoft Online Services](https://support.microsoft.com/kb/2392130).

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx).

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx).

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

