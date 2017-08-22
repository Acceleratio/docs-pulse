---
title: SysKit Pulse - Release Note
description: This article describes all new features, improvements and bug fixes delivered in SysKit Pulse.
author: Hrvoje Bagaric
date: 25/8/2017
---

We’ve shipped __SysKit Pulse__! This is the newest addition to our line of products aimed at monitoring servers. SysKit Pulse is a free tool and we intend to keep it free.

Additional great news is that in these few months, we’ve rebranded our company and Acceleratio officially became SysKit! In recent turn of events, we decided to rebrand our products as well, including SPDocKit Pulse which became SysKit Pulse. Here’s our [official rebranding announcement](https://www.syskit.com/blog/rebranding-announcement-syskit).

SysKit Pulse was developed on the SPDocKit Pulse foundation to add significant performance and user interface improvements. Unfortunately, you cannot upgrade from SPDocKit Pulse to SysKit Pulse.

The tool is developed to discover __SharePoint servers, SQL servers and SQL AlwaysOn configurations__. In case the AutoDiscover job is unable to autodetect all your servers, you can manually add servers as well. For crawling multiple domains or just specific organizational units, use the tool to configure the AutoDiscover job feature according to user’s needs.

Once servers are discovered, SysKit Pulse will monitor basic server metrics such as __CPU__ load, __memory__, __disk__ and __network__ usage. 

__Product version:__ 1.0.0  
__Build number:__   528    
__Release date:__ Aug 25, 2017  


[Click here to download the new release.](https://www.syskit.com/products/pulse#download/)

## Features 

* __Auto Discovery__ - discover all SharePoint servers and farms, as well as SQL servers and SQL AlwaysOn configurations. SysKit Pulse will periodically crawl configured domains to discover new servers.

* __Domain Management__ - This feature allows users to specify where to look for servers. Users can add multiple domains or/and specify Organizational Units for each domain.

* __Add servers manually__ - If the auto discover job is not able to discover all servers in your domain, users can manually add servers. Additionally, users can create server groups (SharePoint, SQL, Custom) as well and monitor them.

* __Server Monitoring__ - Monitor common server metrics for each discovered and added server. With the help of interactive tiles, detect Critical, Warning, Healthy and Offline state for each server. The state is calculated based on the collected values during the last 15 minutes. You can monitor the following metrics:
  * CPU usage – Shows CPU utilization for the last 15 minutes. This value is in shown in percentage. If the value is above 90%, the server will be flagged warning and if it is above 95%, the server will me flagged critical.
  * Memory usage – Shows how much RAM your server is using. If the server has less than 512MB free memory, it will be flagged as warning. If it has less than 256MB free memory, it will be flagged as critical.
  * Disk usage – Monitors Total I/O for disks on each server and free space on each partition. If the partition has less than 3GB of free space the server will be flagged as warning and if there is less than 1GB of free space, the server will be flagged as critical. This check is performed only for partitions larger than 5GB.
  * Network usage – Monitors the total network usage across all network adapters on server.

* __Multiple visualization options__ - SysKit Pulse comes with multiple views. The default __Tiles view__ shows servers with collected metrics. If this view takes too much screen space, there is the __Compact view__ which shows server names only. You can see the tile if you hover over the server name. The __Grid view__ is more structured. You can re-arrange the views as follows:
  * __Smart__ - The default option, will group servers based on AutoDiscover. Servers are grouped by SharePoint farm, SQL AlwaysOn group and all SQL servers are grouped in a separate group.
  * __Type__ - Servers will be grouped by a certain type such as SharePoint Servers, SQL Servers, SQL AlwaysOn Servers groups.
  * __Status__ - Servers will be grouped by their status (warning, critical, healthy, offline).
  * __None__ - Servers will not be grouped.
