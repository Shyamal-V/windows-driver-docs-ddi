---
UID: NF:stiusd.IStiUSD.GetNotificationData
title: IStiUSD::GetNotificationData method
author: windows-driver-content
description: A still image minidriver's IStiUSD::GetNotificationData method returns a description of the most recent event that occurred on a still image device.
old-location: image\istiusd_getnotificationdata.htm
old-project: image
ms.assetid: c4293fa8-07c9-40b2-acc2-8a3128b6dad4
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: stifnc_1641dbac-f429-4f85-9cd0-25ef82000992.xml, IStiUSD::GetNotificationData, IStiUSD interface [Imaging Devices], GetNotificationData method, image.istiusd_getnotificationdata, stiusd/IStiUSD::GetNotificationData, GetNotificationData method [Imaging Devices], IStiUSD interface, GetNotificationData method [Imaging Devices], IStiUSD, GetNotificationData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: stiusd.h
req.include-header: Stiusd.h
req.target-type: Desktop
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
req.lib: stiusd.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	stiusd.h
apiname:
-	IStiUSD.GetNotificationData
product: Windows
targetos: Windows
req.typenames: "*PSTI_WIA_DEVICE_INFORMATIONW, STI_WIA_DEVICE_INFORMATIONW"
req.product: Windows 10 or later.
---

# IStiUSD::GetNotificationData method


## -description


A still image minidriver's <b>IStiUSD::GetNotificationData</b> method returns a description of the most recent event that occurred on a still image device.


## -syntax


````
HRESULT GetNotificationData(
   LPSTINOTIFY pBuffer
);
````


## -parameters




### -param lpNotify






#### - pBuffer

Caller-supplied pointer to an <a href="..\sti\ns-sti-_stinotify.md">STINOTIFY</a> structure to receive event information.


## -returns



If the operation succeeds, the method should return S_OK. Otherwise, it should return one of the STIERR-prefixed error codes defined in <i>stierr.h</i>. If no events have occurred since the last time the method was called, the method should return STIERR_NOEVENTS.




## -remarks



Each time a device event occurs, the still image event monitor calls <b>IStiUSD::GetNotificationData</b> to obtain an event description. These descriptions are added to a linked list and when an application calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff543751">IStiDevice::GetLastNotificationData</a>, the most recent addition to the list is returned.



