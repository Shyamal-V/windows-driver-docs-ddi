---
UID: NI:mountmgr.IOCTL_MOUNTMGR_AUTO_DL_ASSIGNMENTS
title: IOCTL_MOUNTMGR_AUTO_DL_ASSIGNMENTS
author: windows-driver-content
description: This IOCTL informs the mount manager that it should assign drive letters to volumes automatically as they are introduced in the system.
old-location: storage\ioctl_mountmgr_auto_dl_assignments.htm
old-project: storage
ms.assetid: 59ceeaaf-0916-4f0a-a636-624f2f70a64c
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: storage.ioctl_mountmgr_auto_dl_assignments, IOCTL_MOUNTMGR_AUTO_DL_ASSIGNMENTS control code [Storage Devices], IOCTL_MOUNTMGR_AUTO_DL_ASSIGNMENTS, mountmgr/IOCTL_MOUNTMGR_AUTO_DL_ASSIGNMENTS, k307_ec5f9d47-ffd0-481c-8ce9-fa0465c5b69c.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: mountmgr.h
req.include-header: Mountmgr.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	Mountmgr.h
apiname:
-	IOCTL_MOUNTMGR_AUTO_DL_ASSIGNMENTS
product: Windows
targetos: Windows
req.typenames: "*PMOUNTDEV_UNIQUE_ID, MOUNTDEV_UNIQUE_ID"
---

# IOCTL_MOUNTMGR_AUTO_DL_ASSIGNMENTS IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


This IOCTL informs the mount manager that it should assign drive letters to volumes automatically as they are introduced in the system.


## -ioctlparameters




### -input-buffer

None


### -input-buffer-length

None


### -output-buffer

None


### -output-buffer-length

None


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the operation is successful, the <b>Status</b> field is set to STATUS_SUCCESS.

