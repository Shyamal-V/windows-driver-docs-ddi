---
UID: NC:d3dkmthk.PDXGK_REMOVAL_NOTIFICATION
title: PDXGK_REMOVAL_NOTIFICATION
author: windows-driver-content
description: A callback indicating that the graphics device is being removed.
old-location: display\pdxgk_removal_notification.htm
old-project: display
ms.assetid: F9AA5859-8E8A-491D-B149-F42E418A64DC
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.pdxgk_removal_notification, *PDXGK_REMOVAL_NOTIFICATION callback function [Display Devices], *PDXGK_REMOVAL_NOTIFICATION, d3dkmthk/*PDXGK_REMOVAL_NOTIFICATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmthk.h
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
-	UserDefined
apilocation:
-	d3dkmthk.h
apiname:
-	*PDXGK_REMOVAL_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: DXGK_TARGETMODE_DETAIL_TIMING
---

# PDXGK_REMOVAL_NOTIFICATION callback


## -description


A callback indicating that the graphics device is being removed.


## -prototype


````
VOID *PDXGK_REMOVAL_NOTIFICATION(
   PVOID GraphicsDeviceHandle
);
````


## -parameters




### -param GraphicsDeviceHandle

A handle to the graphics device.


### -param PrivateHandle








## -returns



This callback function does not return a value.



