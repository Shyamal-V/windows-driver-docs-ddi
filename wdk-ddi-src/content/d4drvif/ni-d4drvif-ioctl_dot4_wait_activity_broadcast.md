---
UID: NI:d4drvif.IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST
title: IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST
author: windows-driver-content
description: This topic describes IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST.
old-location: print\ioctl_ioctl_dot4_wait_activity_broadcast.htm
old-project: print
ms.assetid: 4E39AC46-BE78-4503-AA3A-D45BC79DBDEF
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: print.ioctl_ioctl_dot4_wait_activity_broadcast, IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST control code [Print Devices], IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST, d4drvif/IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: d4drvif.h
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
-	D4drvif.h
apiname:
-	IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST
product: Windows
targetos: Windows
req.typenames: D3DDDIARG_GETENCRYPTIONBLTKEY
---

# IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


This topic describes <b>IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST</b>.


## -ioctlparameters




### -input-buffer




### -input-buffer-length




### -output-buffer




### -output-buffer-length




### -in-out-buffer




### -inout-buffer-length




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff542894">Creating IOCTL Requests in Drivers</a>



<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendioctlsynchronously.md">WdfIoTargetSendIoctlSynchronously</a>



<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendinternalioctlsynchronously.md">WdfIoTargetSendInternalIoctlSynchronously</a>



<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendinternalioctlotherssynchronously.md">WdfIoTargetSendInternalIoctlOthersSynchronously</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IOCTL_DOT4_WAIT_ACTIVITY_BROADCAST control code%20 RELEASE:%20(2/2/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

