---
UID: NE:d3dumddi._DXVAHDDDI_NOMINAL_RANGE
title: "_DXVAHDDDI_NOMINAL_RANGE"
author: windows-driver-content
description: Indicates the luminance range of YUV data.
old-location: display\dxvahdddi_nominal_range.htm
old-project: display
ms.assetid: 952BE36C-0F53-47C3-9C95-E6ECAB9D36D1
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: DXVAHDDDI_NOMINAL_RANGE_0_255, d3dumddi/DXVAHDDDI_NOMINAL_RANGE_UNDEFINED, _DXVAHDDDI_NOMINAL_RANGE, display.dxvahdddi_nominal_range, DXVAHDDDI_NOMINAL_RANGE, d3dumddi/DXVAHDDDI_NOMINAL_RANGE, DXVAHDDDI_NOMINAL_RANGE_UNDEFINED, DXVAHDDDI_NOMINAL_RANGE_16_235, DXVAHDDDI_NOMINAL_RANGE enumeration [Display Devices], d3dumddi/DXVAHDDDI_NOMINAL_RANGE_16_235, d3dumddi/DXVAHDDDI_NOMINAL_RANGE_0_255
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
-	D3dumddi.h
apiname:
-	DXVAHDDDI_NOMINAL_RANGE
product: Windows
targetos: Windows
req.typenames: DXVAHDDDI_NOMINAL_RANGE
---

# _DXVAHDDDI_NOMINAL_RANGE enumeration


## -description


Indicates the luminance range of YUV data.


## -syntax


````
typedef enum _DXVAHDDDI_NOMINAL_RANGE { 
  DXVAHDDDI_NOMINAL_RANGE_UNDEFINED  = 0,
  DXVAHDDDI_NOMINAL_RANGE_16_235     = 1,
  DXVAHDDDI_NOMINAL_RANGE_0_255      = 2
} DXVAHDDDI_NOMINAL_RANGE;
````


## -enum-fields




### -field DXVAHDDDI_NOMINAL_RANGE_UNDEFINED

The driver default value, which is the <i>studio luminance range</i> of 16 to 235, inclusive [16, 235].


### -field DXVAHDDDI_NOMINAL_RANGE_16_235

The <i>studio luminance range</i> of 16 to 235, inclusive [16, 235].


### -field DXVAHDDDI_NOMINAL_RANGE_0_255

The <i>full luminance range</i>, or <i>extended range</i>, of 0 to 255, inclusive [0, 255].


## -remarks



For more information on luminance range, see <a href="https://msdn.microsoft.com/D76FFB8C-CA42-446E-826F-52982B1849E5">YUV format ranges in Windows 8.1</a>.



