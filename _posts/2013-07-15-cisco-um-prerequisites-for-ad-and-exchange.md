---
layout: post
title: Cisco UM Prerequisites for AD and Exchange
comments: true
date: 2013-07-15
description: cisco um prerequisites for ad and exchange
keywords: powershell, exchange, cisco uc
categories:
    - powershell
    - script
    - interactive
    - reference
tags:
    - exchange
    - ad
    - cisco
    - messaging
slug: cisco-um-prerequisites-ad-exchange
---

A few AD and Exchange prerequisites required for Cisco Unified Messaging service[[^1]].  After SP2 RU3 Exchange throttling policies moved to the mailbox level, so script was required for proper setup.

{% gist jbilinski/45dd262164225e19ccca36b41eb46a47 cisco-um-prerequisites-for-ad-and-exchange-1.ps1 %}

---

References:

[^1]: 1: Cisco UC reference [https://www.cisco.com/en/US/docs/voice_ip_comm/connection/8x/unified_messaging/guide/85xcucumg020.html#wp1195262](https://www.cisco.com/en/US/docs/voice_ip_comm/connection/8x/unified_messaging/guide/85xcucumg020.html#wp1195262)

