---
title: SysKit Pulse - Release Note
description: This article describes all new features, improvements and bug fixes delivered in SysKit Pulse.
author: Hrvoje Bagaric
date: 7/6/2017
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

* __Manual server addition__ - If the auto discover job does not find some servers, users can manually add servers. Additionaly to adding servers, users can create server groups (SharePoint, SQL, Custom) to monitor.

* __Server Monitoring__ - SysKit Pulse monitors general server metrics for each discovered and added server. It will detect Critical, Warning, Healthy and Offline state for each server. The state is calculated based on the collected values during the last 15 minutes.
Monitored metrics are:
  * CPU usage - Percentage usage of CPU during the last 15 minutes. If the value is above 90% server will enter warning state, and if it is above 95% server will enter critical state.
  * Memory usage - Memory (RAM) used on server. If there is less than the 512MB of free memory the server will enter warning state and if there is less than 256MB the server will enter critical state.
  * Disk usage - SysKit Pulse will monitor Total I/O for disks on each server as well as free space on each partition. If there is less than 3GB of free space on partition the server will enter warning state and if there is less than 1GB of free space on partiton the server will enter the critical state. This check is performed only on partitions larger than 5GB.
  * Network usage - SysKit Pulse will monitor total network usage accross all network adapters on server.

* __Multiple visualization options__ - SysKit Pulse comes with multiple views to show the servers. The default __Tiles view__ shows servers and its collected metrics. If this view takes too much of screen space, there is __Compact view__ which shows only the server names. On hover the tile for the server is shown. __Grid view__ is there for more structured approach.
Additionally users can define grouping: 
  * __Smart__ - The default option, will group servers based on AutoDiscover. Servers are grouped by SharePoint farm, SQL AlwaysOn group and all SQL servers are grouped in seperate group.
  * __Type__ - Servers will be SharePoint Servers, SQL Servers, SQL AlwaysOn Servers groups.
  * __Status__ - Servers will be grouped base on their state.
  * __None__ - Servers will not be grouped.

