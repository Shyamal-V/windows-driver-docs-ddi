---
UID: NI:ntdddisk.IOCTL_DISK_FIND_NEW_DEVICES
title: IOCTL_DISK_FIND_NEW_DEVICES
author: windows-driver-content
description: In Microsoft Windows 2000 and later operating systems, this IOCTL is replaced by IOCTL_STORAGE_FIND_NEW_DEVICES. The only difference between the two IOCTLs is the base value.
old-location: storage\ioctl_disk_find_new_devices.htm
old-project: storage
ms.assetid: d8a603a3-fa3c-4524-89f8-eed43d0db316
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: storage.ioctl_disk_find_new_devices, IOCTL_DISK_FIND_NEW_DEVICES control code [Storage Devices], IOCTL_DISK_FIND_NEW_DEVICES, ntdddisk/IOCTL_DISK_FIND_NEW_DEVICES, k307_369ae687-ba0c-4626-bd33-eb299ab4c2cd.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntdddisk.h
req.include-header: TBD
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
-	ntdddisk.h
apiname:
-	IOCTL_DISK_FIND_NEW_DEVICES
product: Windows
targetos: Windows
req.typenames: DETECTION_TYPE
---

# IOCTL_DISK_FIND_NEW_DEVICES IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


In Microsoft Windows 2000 and later operating systems, this IOCTL is replaced by <a href="..\ntddstor\ni-ntddstor-ioctl_storage_find_new_devices.md">IOCTL_STORAGE_FIND_NEW_DEVICES</a>. The only difference between the two IOCTLs is the base value.


## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [XREF-LINK:NTSTATUS Values].



