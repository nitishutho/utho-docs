---
title: "How to Turn off Internet Explorer Enhanced Security Configuration on Windows Server"
date: "2022-09-26"
Title_meta: GUIDE TO Turn off Internet Explorer Enhanced Security Configuration on Windows Server

Description: This guide provides step-by-step instructions on how to disable Internet Explorer Enhanced Security Configuration (IE ESC) on Windows Server. Learn how to navigate Server Manager, adjust IE ESC settings for administrators and users, and improve browsing flexibility while maintaining security standards.

Keywords: ['Internet Explorer Enhanced Security Configuration', 'Windows Server', 'disable IE ESC', 'Server Manager', 'browser security settings']

Tags: ["Internet Explorer Enhanced Security Configuration", "Windows Server", "Disable IE ESC", "Server Manager", "Browser Security Settings"]
icon: "windows"
date: "2024-03-07T17:25:05+01:00"
lastmod: "2024-03-07T17:25:05+01:00" 
draft: false
toc: true
aliases: ['/Windows/how-to-turn-off-internet-explorer-enhanced-security-configuration-on-windows-server']
tab: true
---

![Turn off Internet Explorer Enhanced Security](images/How-to-Turn-off-Internet-Explorer-Enhanced-Security-Configuration-on-Windows-Server_utho.jpg)

## Introduction

Internet Explorer [Enhanced Security Configuration](https://learn.microsoft.com/en-us/troubleshoot/developer/browsers/security-privacy/enhanced-security-configuration-faq) (ESC) **establishes security settings that define how users browse the internet and intranet websites**. These settings also reduce the exposure of servers to websites that might present a security risk. This process is also known as IEHarden.

Step 1. Connect to your Windows server with Remote Desktop Protocol (RDP).

Step 2. Open **[Server Manager](https://utho.com/docs/tutorial/how-to-setup-ssh-server-on-windows-server-via-powershell/)** from the Windows start menu.

![](images/Screenshot_1-20-1024x542.png)

Step 3. Open Local Server

![Turn off Internet Explorer Enhanced Security](images/Screenshot_2-26.png)

Step 4. Click on "**IE Enhanced Security Configuration**" property in the right-hand panel, and click on "**ON"**

![](images/Screenshot_3-20-1024x374.png)

step 5. Click on Turn the option **"off"** for Administrators and Users, then click "**OK**"

![Turn off Internet Explorer Enhanced Security](images/Screenshot_4-23.png)

Step 6. Select **refresh** on the Server Manager toolbar for changes to take effect.

![](images/Screenshot_5-18-1024x348.png)

Step 7. Server Manager will now show **"off**" for the IE Enhanced Security Configuration property, and you will be able to browse the web without any warnings in Internet Explorer.

![Turn off Internet Explorer Enhanced Security](images/Screenshot_6-16-1024x357.png)

Thank You.
