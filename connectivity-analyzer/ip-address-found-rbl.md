---
title: IP Address Found on RBL
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The IP X.X.X.X was found on the block list. Status code: X'
ms.date: 05/08/2020
---

# IP Address Found on RBL


_**Topic Last Modified:** 2012-03-26_

The Microsoft Remote Connectivity Analyzer checks the provided outbound IP address against several real-time block lists (RBLs) as part of its Outbound SMTP test. When the IP address provided is found on one or more RBLs, you receive the following error message:


<table>
<colgroup>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>The IP X.X.X.X was found on the block list. Status code: X</p></td>
</tr>
</tbody>
</table>

<div>

## For More Information

RBLs are also known as DNSBLs (DNS-based block lists or "blackhole" lists) because they are based on the well-known DNS protocol. RBLs are lists of IP addresses that are published through DNS and that are believed to be known sources of spam either actively, through incorrect configuration, through malware infection, or otherwise.

Many parties on the Internet publish and maintain these lists for others to use in a defense against spam. However, it is also possible to locate these lists unintentionally.

As part of the Microsoft Remote Connectivity Analyzer (ExRCA) outbound SMTP test, the ExRCA checks your IP address against some well-known RBLs to see whether it is listed. If your IP address is listed, ExRCA sends you an error message that resembles the message in the "Introduction" section. The message will include the name of the RBL and the status code.

RBL servers typically return an error code in the form of a loop-back address, such as 127.0.0.2. The last octet in the loop-back address defines the error code, which is "2" in this case. The meanings of the codes vary between RBL providers. You have to review the Web site of the list provider to find the exact meaning of the code. This also applies to posting a request to be removed from an RBL.

Typical codes include the following:

  - **127.0.0.2** - known open relay

  - **127.0.0.3** - dial-up-issued address or DHCP-issued address

<div>

## What this error means to you as an admin

Many e-mail servers use popular RBLs as one defense against spam. If the IP address of your Exchange Server appears on an RBL to which a receiving server is subscribed, mail from your domain may be rejected or flagged as spam. It is for this reason that ExRCA tries to detect the presence of the IP address that you entered against some of these more well know RBLs.

To see examples of some well-known RBLs, visit the following Web sites:

  - <https://www.dnsbl.info/dnsbl-details.php?dnsbl=pbl.spamhaus.org>

  - <https://www.au.sorbs.net/>

  - <https://www.spamcop.net/>

For more information about RBLs, see Configuring Filtering and Controlling Spam and also visit the following Spam Links Web site:

  - <https://spamlinks.net/filter-dnsbl-lists.htm>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

