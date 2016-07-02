---
layout: post
title: "New daily password and a Cisco guest wireless portal"
comments: true
date: "2014-05-19"
description: "new daily password and a cisco guest wireless portal"
keywords: "cisco, wireless, guest portal"
categories: [powershell, script, automation]
tags: [cisco, wireless, guest]
---

> Update: This method has worked very well for a couple years now.  I should probably expand on this post and I would like to try using new windows/powershell OpenSSH code instead of CatTools.

This script is being used to implement a wireless guest portal with a semi-random password and update an internal website with the current password.

Here's what I had to work with:

* Windows Server
* Webserver (IIS)
* Cisco Wireless Lan Controllers  [[^1]]
* Existing router config managment tool (CatTools)  [[^2]]


Here's the full script

{% gist jbilinski/ef5234fdba85289a68f32a5ecaafc4d0 new-daily-password-and-a-cisco-guest-wireless-portal-1.ps1 %}

References
[^1]: 1: Cisco WLC reference [http://www.cisco.com/c/en/us/products/wireless/wireless-lan-controller/index.html](http://www.cisco.com/c/en/us/products/wireless/wireless-lan-controller/index.html)
[^2]: 2: Kiwi CatTools reference [http://www.solarwinds.com/kiwi-cattools.aspx](http://www.solarwinds.com/kiwi-cattools.aspx)




