---
title: Missing EXPR Element in Autodiscover XML Response
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: Learn about the "Missing EXPR element in Autodiscover XML Response" error
ms.date: 05/08/2020
---

# Missing EXPR Element in Autodiscover XML Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-02-10_

The Microsoft Remote Connectivity Analyzer queries the HTTP response from the Autodiscover service to determine the attributes contained in the XML within that response. Two Outlook Providers and their attributes are commonly found in the XML:

  - **EXCH Provider**  
    The connection settings and Exchange services URLs used when Outlook connects using RPC.

<!-- end list -->

  - **EXPR Provider**  
    The connection settings and Exchange services URLs used when Outlook connects using HTTP (Outlook Anywhere).

If the EXPR element is missing from the Autodiscover response, then the Microsoft Remote Connectivity Analyzer tool displays the following error message:

"Missing EXPR element in Autodiscover XML Response."

This typically means that Outlook Anywhere is either not enabled or configured correctly.

<div>

## For More Information

  - For more information about deploying Outlook Anywhere, see [Deploying Outlook Anywhere](https://go.microsoft.com/fwlink/?linkid=80831).

  - For more information about the Outlook Providers, see [The Autodiscover Service and Outlook Providers - how does this stuff work?](https://go.microsoft.com/fwlink/?linkid=161811)

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

