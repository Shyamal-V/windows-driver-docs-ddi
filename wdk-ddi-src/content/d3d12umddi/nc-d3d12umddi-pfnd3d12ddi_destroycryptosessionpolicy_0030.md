---
UID: NC:d3d12umddi.PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030
title: PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030
author: windows-driver-content
description: Used to destroy a crypto session.
old-location: display\pfnd3d12ddi_destroycryptosessionpolicy_0030.htm
old-project: display
ms.assetid: D02ED6F5-1976-4EAE-A648-0F8ED32B77C6
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.pfnd3d12ddi_destroycryptosessionpolicy_0030, PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030 callback function [Display Devices], PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030, d3d12umddi/PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d12umddi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
-	d3d12umddi.h
apiname:
-	PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030
product: Windows
targetos: Windows
req.typenames: D3D11_1DDI_GETCAPTUREHANDLEDATA
---

# PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030 callback


## -description


Used to destroy a crypto session.


## -prototype


````
VOID APIENTRY* PFND3D12DDI_DESTROYCRYPTOSESSIONPOLICY_0030(
   D3D12DDI_HDEVICE                   hDrvDevice,
   D3D12DDI_HCRYPTOSESSIONPOLICY_0030 hDrvCryptoSessionPolicy
);
````


## -parameters




### -param hDrvDevice

The hardware device being processed.


### -param hDrvCryptoSessionPolicy

The crypto session policy.


## -returns



This callback function does not return a value.



