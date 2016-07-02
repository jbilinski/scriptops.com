---
layout: post
title: "Flush stale Jabber contact cache"
comments: true
date: "2014-05-07"
description: "flush stale jabber contact cache"
keywords: "cisco, jabber, stale contacts"
categories: [powershell, script, interactive]
tags: [jabber, cisco, contacts]
---

Some versions of Cisco Jabber have an issue updating contacts that are stored in the local cache.
Here's my quick solution to resolve that issue when it arrises.

{% gist jbilinski/424238345dc72000ec7d93dc840282d8 flush-stale-jabber-contact-cache-1.ps1 %}

The script finds the contact cache, stops the Jabber process, makes a backup copy of cache, then restarts Jabber.
