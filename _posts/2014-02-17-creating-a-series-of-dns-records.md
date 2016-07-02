---
layout: post
title: "Creating a series of DNS records"
comments: true
date: "2014-02-17"
description: "creating a series of dns records"
keywords: "powershell, windows, dns"
categories: [powershell, script, interactive, automation]
tags: [microsoft, server , dns]
---

When standing up a new grid or cluster, static DNS records are often required. This example script will add A and in-arpa records for 20 hosts (*ava-ks-1* to *ava-ks-20*) and map sequential, even-numbered, IP addresses starting with *10.111.160.40*. 

{% gist jbilinski/73694c61e98d898555a060cd4243233d creating-a-series-of-dns-records-1.ps1 %}
