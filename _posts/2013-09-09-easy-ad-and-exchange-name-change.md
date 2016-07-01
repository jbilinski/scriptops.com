---
layout: post
title: "Easy AD and Exchange name change"
comments: true
date: "2013-09-09"
description: "easy ad and exchange name change"
keywords: "powershell, exchange, ad, rename"
categories: [powershell, script, interactive, reference]
tags: [exchange, ad]
---
I often get requests for name changes of established customers. Maintaining the old records as an alias is easy if using an address policy. Here's how I like to do this:

{% gist jbilinski/db260a808ec27207b331594318680239 easy-ad-and-exchange-name-change-1.ps1 %}

The Disable and Enable of the address policy corrects the email address by adding the new rules.

Old addresses are preserved, new ones are added:

```PowerShell
(get-mailbox jbilinski).emailaddresses

SIP:jamie.bilinski@Contoso.com
sip:jan.bilinski@Contoso.com
smtp:JBilinski@TX.Contoso.com
X400:C=US;A= ;P=Contoso;O=Exchange;S=Bilinski;G=Jamie;I=JCB;
x400:C=US;A= ;P=Contoso;O=Exchange;S=Bilinski;G=Jan;I=JCB;
SMTP:Jamie.Bilinski@Contoso.com
smtp:Jan.Bilinski@Contoso.com

```

