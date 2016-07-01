---
layout: post
title: "Add Exchange resource mailbox delegate"
comments: true
date: "2013-10-16"
description: "add exchange resource mailbox delegate"
keywords: "powershell, exchange, resource mailbox"
categories: [powershell, script, interactive, reference]
tags: [exchange, resource mailbox, delegate]
---

This example will add resource mailbox delegate to all existing *RoomMailbox* recipients that start with the string *CargoHold*.

Unfortunately, the hashtable *add* method [here]{% post_url 2013-10-14-powershell-syntax-using-add-and-remove-keyword-methods %}
 is not supported by the `Set-CalendarProcessing` command.

{% gist jbilinski/eccc3e6cb35acd51481e52e5f2f1e094 add-exchange-resource-mailbox-delegate-1.ps1 %}

