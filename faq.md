# FAQ

## How does the SysKit Insights Lite work?

SysKit Insights Lite discovery module relies on two things: 1. SysKit Insights Lite relies on Active Directory to reach the names/addresses of the computer. So, the permission to read from AD is required. 2. After that, it uses WMI to search the registry and collect all the data from the SharePoint servers. Classic WMI TCP/UDP ports are used.

## What is the connection between SysKit Insights Lite and SPDocKit Pulse?

SysKit Insights Lite is a successor to SPDocKit Pulse. SysKit Insights Lite retains all features of SPDocKit Pulse while adding a few more. SysKit Insights Lite is more optimized and performant. Unfortunately due to technical issues it is not possible to upgrade from SPDocKit Pulse to SysKit Insights Lite.

## Does the SysKit Insights Lite product have to be installed on a server or can I install it on my desktop?

SysKit Insights Lite can be installed either on a server or on a desktop. Actually, we recommend that you install it on a desktop in the same domain as the SharePoint servers that you wish to monitor.

## Does SysKit Insights Lite work from a workstation or the server?

SysKit Insights Lite works from a workstation as well as from a server. We recommend that you run it from a workstation.

## Is it possible to add a SharePoint farm manually to a SysKit Insights Lite dashboard?

Yes, you can manually add a SharePoint farm to a SysKit Insights Lite dashboard.

## Could you tell us the default thresholds for performance counters?

* CPU - If the value is above 85%, the server will be flagged as warning and if it is above 95%, the server will be flagged critical.
* Memory usage – If the server has less than 512MB free memory, it will be flagged as warning. If it has less than 256MB free memory, it will be flagged as critical.
* Disk usage – If the partition has less than 3GB of free space the server will be flagged as warning and if there is less than 1GB of free space, the server will be flagged as critical. This check is performed only for partitions larger than 5GB.

