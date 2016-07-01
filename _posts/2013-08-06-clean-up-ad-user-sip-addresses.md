---
layout: post
title: "Clean-up AD user SIP addresses"
comments: true
date: "2013-08-06"
description: "clean up ad user sip addresses"
keywords: "powershell, exchange, sip"
catagories: [powershell, script, interactive, reference]
tags: [exchange, ad, sip, uc]
---
Here's a method I used during a new UC rollout to make a one-time pass in AD to clean-up inconsistent or missing SIP addresses.
I found it useful later to ID and correct "broken" accounts.

{% gist jbilinski/15fa6dc5ad7cdda47c4e3e2b6cd22fc4 clean-up-ad-user-sip-addresses-1.ps1 %}

