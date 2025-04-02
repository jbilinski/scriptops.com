---
layout: post
title: Install CA and Subordinates on MacOS
comments: true
date: 2017-09-21
description: Script to install a corporate CA and subordinate CA on MacOS
keywords: macos, ca, certificate
categories:
    - powershell
    - tool
    - script
    - build
    - reference
tags:
    - bash
    - macos
    - ca
    - certificate
slug: install-ca-subordinates-macos
---
This is a quick fix I wrote for developers to install internal root and subordinate CAs.
It pulls the root certificate from a web server, verifies the fingerprint, parses and downloads subordinates, and installs them in the MacOS keychain.  It was intended to be run interactively at the command line, but also works well as a machine setup script.

The thumbprint verification is required to prevent malicious endpoints. Since the CA server is, in this case, is a windows CA server and signed by the same root, an insecure `curl -k` is used leaving the user open to a xITM attack.  The thumbprint is a hash of the certificate with a very low probability of collision.

{% gist jbilinski/b7b6aa670c3bdd807c924c19fff74478 install-corp-ca-macos.sh %}

### Tips
- if your https endpoint is signed by a pre-installed MacOS CA, please remove `-k` from the curl command.

### References
- [Apple Keychain](https://developer.apple.com/library/content/documentation/Security/Conceptual/certkeychainguide/Introduction/Introduction.html)
- [MacOS Security Command](https://ss64.com/mac/security.html)
