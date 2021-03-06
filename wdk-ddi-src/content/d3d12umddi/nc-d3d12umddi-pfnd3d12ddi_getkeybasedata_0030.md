---
UID: NC:d3d12umddi.PFND3D12DDI_GETKEYBASEDATA_0030
title: PFND3D12DDI_GETKEYBASEDATA_0030
author: windows-driver-content
description: Used to get key base data.
old-location: display\pfnd3d12ddi_getkeybasedata_0030.htm
old-project: display
ms.assetid: D4F893E9-6B7B-4E35-A92F-B31FFD55A2C0
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.pfnd3d12ddi_getkeybasedata_0030, PFND3D12DDI_GETKEYBASEDATA_0030 callback function [Display Devices], PFND3D12DDI_GETKEYBASEDATA_0030, d3d12umddi/PFND3D12DDI_GETKEYBASEDATA_0030
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d12umddi.h
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
-	d3d12umddi.h
apiname:
-	PFND3D12DDI_GETKEYBASEDATA_0030
product: Windows
targetos: Windows
req.typenames: D3D11_1DDI_GETCAPTUREHANDLEDATA
---

# PFND3D12DDI_GETKEYBASEDATA_0030 callback


## -description


Used to get key base data.


## -prototype


````
HRESULT APIENTRY* PFND3D12DDI_GETKEYBASEDATA_0030(
              D3D12DDI_HDEVICE             hDrvDevice,
              D3D12DDI_HCRYPTOSESSION_0030 hDrvCryptoSession,
  _In_  const VOID                         *pKeyInputData,
              UINT                         KeyInputDataSize,
  _Out_       VOID                         *pKeyBaseData,
              UINT                         KeyBaseDataSize
);
````


## -parameters




### -param hDrvDevice

The device being processed.


### -param hDrvCryptoSession

The crypto session.


### -param *pKeyInputData [in]

A pointer to key input data.


### -param KeyInputDataSize

The size of the key input data.


### -param *pKeyBaseData [out]

A pointer to key base data.


### -param KeyBaseDataSize

The size of the key base data.


## -returns



Returns STATUS_SUCCESS if completed successfully.



