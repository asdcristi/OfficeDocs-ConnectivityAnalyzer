---
title: SSL Certificate Trust Failure
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: SSL Certificate trust failure
ms.date: 05/08/2020
---

# SSL Certificate Trust Failure

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-06-21_

The Microsoft Remote Connectivity Analyzer Tool queries the Server Certificate object in the Exchange Server system to retrieve various properties on X509 certificates. In order for the Remote Connectivity Analyzer to validate a given X509 certificate, the toll must trust the root Certificate Authority (CA) that issued the certificate. If the tool cannot follow the certificate chain to the trusted root, it displays an error indicating that the certificate is not trusted.

This issue typically occurs when the Web server certificate on the Client Access server is a self-signed certificate or one that was created by using a private or internal PKI. This issue can also occur if certificates are chained to a CAS by another intermediate certificate. Every certificate in the certification path must be valid for the certificate to be valid.

Common symptoms of this issue include the following:

  - Users are repeatedly prompted for credentials and cannot successfully connect by using Outlook Anywhere.

  - Users who try to connect to Outlook Web Access receive the following error message: "There is a problem with this website's security certificate."

The Remote Connectivity Analyzer has the ability to ignore the trust requirement during SSL certificate validation for most tests. However, the Outlook Anywhere (RPC over HTTP) connectivity tests currently require a publicly-trusted certificate that is also trusted by the server.

If you are running the Microsoft Office 365 Single Sign-on test, you may experience a similar issue in which users are continuously prompted for credentials when they try to access the Office 365 services. The Remote Connectivity Analyzer queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. The endpoint is a Secure Sockets Layer (SSL) connection, which will have a certificate in place. The Remote Connectivity Analyzer evaluates the fully qualified domain name (FQDN) that was assigned to the certificate. For example, the tool evaluates STS.Contoso.com.

The Remote Connectivity Analyzer displays a warning if the certificate that is used for SSL cannot be trusted up to the root. This message indicates that the certificate is not a certificate that is trusted by the Office 365 environment. In many cases, this error occurs because the certificate is a self-signed certificate that is not valid for this kind of authentication. To resolve this issue for the Single Sign-On test, see Microsoft Knowledge Base article 2523494, [You receive a certificate warning when you try to access Microsoft Office 365 resources by using an identity-federated account](https://support.microsoft.com/kb/2523494)

<div>

## For More Information

For more information about certificates and validation, see the following topics.

  - For more information about using certificates for securing communications between a client and Client Access server, see [Understanding SSL for Client Access Servers](https://go.microsoft.com/fwlink/?linkid=115184).

  - For more information about the use of certificates in Exchange Server 2007, see [Certificate Use in Exchange Server 2007](https://go.microsoft.com/fwlink/?linkid=119030).

  - For more information about self-signed certificates in Exchange Server 2007, see [Understanding the Self-Signed Certificate in Exchange 2007](https://go.microsoft.com/fwlink/?linkid=161990).

  - For more information about using third-party and private certificate authorities when planning to deploy Autodiscover, see the [White Paper: Exchange 2007 Autodiscover Service](https://go.microsoft.com/fwlink/?linkid=157773).

</div>

</div>

<span> </span>

</div>

</div>

</div>

