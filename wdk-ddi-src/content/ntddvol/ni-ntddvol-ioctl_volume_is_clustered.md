---
UID: NI:ntddvol.IOCTL_VOLUME_IS_CLUSTERED
title: IOCTL_VOLUME_IS_CLUSTERED
author: windows-driver-content
description: Allows a driver or application to determine if a volume is clustered.
old-location: storage\ioctl_volume_is_clustered.htm
old-project: storage
ms.assetid: aa8accf8-79c9-4868-b621-d468a121cb60
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: storage.ioctl_volume_is_clustered, IOCTL_VOLUME_IS_CLUSTERED control code [Storage Devices], IOCTL_VOLUME_IS_CLUSTERED, ntddvol/IOCTL_VOLUME_IS_CLUSTERED, k307_32e3c9a5-1828-4fbb-b7f1-9ddbd367f70f.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddvol.h
req.include-header: Ntddvol.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows XP.
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
-	Ntddvol.h
apiname:
-	IOCTL_VOLUME_IS_CLUSTERED
product: Windows
targetos: Windows
req.typenames: "*PVIDEO_WIN32K_CALLBACKS_PARAMS, VIDEO_WIN32K_CALLBACKS_PARAMS"
---

# IOCTL_VOLUME_IS_CLUSTERED IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


Allows  a driver or application to determine if a volume is clustered.


## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

None.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

 If the volume is clustered, the IOCTL returns <b>STATUS_SUCCESS</b>. If the volume is not clustered, the IOCTL returns  <b>STATUS_UNSUCCESSFUL</b>.


## -remarks



For an invalid disk type, such as dynamic disk, the disk management component will return <b>STATUS_INVALID_DEVICE_REQUEST</b>.



