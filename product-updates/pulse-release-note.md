---
title: SysKit Pulse - Release Note
description: This article describes all new features, improvements and bug fixes delivered in SysKit Pulse.
author: Hrvoje Bagaric
date: 7/6/2017
---

We have just shipped the __SysKit Pulse__. This is the newest addition to our line of products aimed at monitoring servers. SysKit Pulse is completly free to use tool and it will stay that way!

Our company name has been changed from __Acceleratio__ to __SysKit__! We have also decided to rebuild __SPDocKit Pulse__. The SysKit Pulse builds upon foundation of SPDocKit Pulse and adds significant performance and user interface improvments. There is no upgrade from SPDocKit Pulse to SysKit Pulse.
You can read the back story to these changes in the [Rebranding Announcement](https://www.syskit.com/blog/rebranding-announcement-syskit) blog post.

SysKit Pulse builds upon foundation of our free tool __SPDocKit Pulse__ and delivers capability to discover __SharePoint__ servers and farms. Additionaly SysKit Pulse is able to discover __SQL__ servers and even __SQL AlwaysOn__ configurations. If AutoDiscover job misses some servers, SysKit Pulse allows __manual addition__ of servers.

If there is need to crawl multiple domains, or just specific Organizational Units, SysKit Pulse allows users to configure AutoDiscover job according to their needs. 

Once servers are discovered SysKit Pulse will monitor basic server metrics, __CPU__ load, __memory__, __disk__ and __network__ usage. 

__Product version:__ 1.0.0  
__Build number:__   528    
__Release date:__ Aug 25, 2017  


[Click here to download the new release.](https://www.syskit.com/products/pulse#download/)

## Features 

* __Auto Discovery__ - SysKit Pulse is able to discover all SharePoint servers and farms as well as SQL servers and SQL AlwaysOn configurations. SysKit Pulse will periodically crawl configured domains to discover new servers.

* __Domain Management__ - SysKit Pulse allow users to specify where to look for servers. Users can add multiple domains or/and specify Organizational Units for each domain. 

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

