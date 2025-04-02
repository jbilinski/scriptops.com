---
layout: post
title: Start Jenkins Agent as a Windows Scheduled Job
comments: true
date: 2019-04-28
description: start jenkins agent as a windows scheduled job
keywords: jenkins, windows, agent, pipeline
categories:
    - powershell
    - tool
    - script
    - build
    - reference
tags:
    - jenkins
    - agent
    - windows
slug: start-jenkins-agent-windows-scheduled-job
---

Running a Jenkins agent on a windows build machine can be unstable at restart or lack needed rights. In some cases you require a console session for interaction with policy restricted hardware. Or, the service wrapper limits JVM rights in a way that prevents compilers or test suites from running. 

In these cases, PowerShell scheduled jobs module has a useful _AtStartup_ trigger property as well as a _RunElevated_ job option. 

{% gist jbilinski/be57127fd4dc9f31aa045aec83e6f45f start-jenkins-agent-as-windows-scheduled-job.ps1 %}

### Tips:
 - Add '-noCertificateCheck' java argument if you use a jenkins job to bootstrap agent chain of trust. 
 - Change pipeline and java log to path or file name of your choice.
 - I have seen long windows update restarts interfere with the _AtStartup_ trigger. Adding a contingency trigger will help in this case. 
 - *"kick the can" and move the shared secret to a "secure" variable, file, or registry key. Please leave feedback if you have a better solution. 

### References:
 - [Jenkins Agent](https://jenkins.io/doc/book/agents/)
 - [PowerShell Scheduled Jobs](https://docs.microsoft.com/en-us/powershell/module/psscheduledjob/)
 - [Scheduled Job Trigger Parameters](https://learn.microsoft.com/en-us/powershell/module/psscheduledjob/new-jobtrigger/#parameters)
 - [Java Arguments](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/java.html)
