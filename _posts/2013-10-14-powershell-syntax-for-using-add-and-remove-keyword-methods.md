---
layout: post
title: "PowerShell syntax for using add and remove keyword methods"
comments: true
date: "2013-10-14"
description: "powershell syntax for using add and remove keyword methods"
keywords: "powershell, syntax, hash table"
categories: [powershell, script, interactive, reference]
tags: [example, hash table]
---

Here's an example for using the obscure *add* and *remove* keyword methods for modifying a hash table. This is a supported method for changing an exchange mailbox email address. 

```PowerShell
Set-Mailbox -Identity jsnover -EmailAddresses @{add = 'jeffery.snover@riverlive.com';remove = 'jeff.snover@riverlive.com'}
```