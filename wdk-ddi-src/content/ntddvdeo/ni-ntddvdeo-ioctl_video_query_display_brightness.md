---
UID: NI:ntddvdeo.IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
title: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
author: windows-driver-content
description: This IOCTL is not handled by video miniport drivers. It is handled entirely by the system-supplied video port driver.
old-location: display\ioctl_video_query_display_brightness.htm
old-project: display
ms.assetid: 8dccc5bd-c678-4c94-9fa6-c5ac37ad6d0e
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.ioctl_video_query_display_brightness, IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS control code [Display Devices], IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS, ntddvdeo/IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS, Video_IOCTLs_f55cce8d-9a8e-45ef-98e2-8cabc27cd9e6.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddvdeo.h
req.include-header: 
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
-	Ntddvdeo.h
apiname:
-	IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
product: Windows
targetos: Windows
req.typenames: TAPE_WRITE_MARKS, *PTAPE_WRITE_MARKS
---

# IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description



This IOCTL is not handled by video miniport drivers. It is handled entirely by the system-supplied video port driver.




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




## -remarks



<div class="alert"><b>Note</b>    This IOCTL is obsolete in Windows Vista. Instead, use the Windows Management Instrumentation (WMI) monitor brightness class. For information about WMI, see the documentation in the Microsoft Windows SDK.</div>
<div> </div>


