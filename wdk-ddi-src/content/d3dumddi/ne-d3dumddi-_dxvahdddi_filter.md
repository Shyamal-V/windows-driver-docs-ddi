---
UID: NE:d3dumddi._DXVAHDDDI_FILTER
title: "_DXVAHDDDI_FILTER"
author: windows-driver-content
description: The DXVAHDDDI_FILTER enumeration contains values that identify the filter range, which the driver should retrieve when the driver's GetCaps function is called with the D3DDDICAPS_DXVAHD_GETVPFILTERRANGE value set.
old-location: display\dxvahdddi_filter.htm
old-project: display
ms.assetid: dbf65c28-b4f2-4930-8d01-050c45f87bb4
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: d3dumddi/DXVAHDDDI_FILTER_HUE, d3dumddi/DXVAHDDDI_FILTER_NOISE_REDUCTION, DXVAHDDDI_FILTER_EDGE_ENHANCEMENT, d3dumddi/DXVAHDDDI_FILTER_EDGE_ENHANCEMENT, _DXVAHDDDI_FILTER, DXVAHDDDI_FILTER enumeration [Display Devices], d3dumddi/DXVAHDDDI_FILTER, DXVAHDDDI_FILTER_ANAMORPHIC_SCALING, DXVAHDDDI_FILTER_SATURATION, DXVAHDDDI_FILTER_CONTRAST, d3dumddi/DXVAHDDDI_FILTER_CONTRAST, DXVAHDDDI_FILTER, DXVA2_Structs_730202a4-96bd-4779-b952-d493295f06ad.xml, display.dxvahdddi_filter, d3dumddi/DXVAHDDDI_FILTER_BRIGHTNESS, DXVAHDDDI_FILTER_NOISE_REDUCTION, d3dumddi/DXVAHDDDI_FILTER_ANAMORPHIC_SCALING, d3dumddi/DXVAHDDDI_FILTER_SATURATION, DXVAHDDDI_FILTER_BRIGHTNESS, DXVAHDDDI_FILTER_HUE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Windows
req.target-min-winverclnt: DXVAHDDDI_FILTER is supported beginning with the Windows 7 operating system.
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
-	d3dumddi.h
apiname:
-	DXVAHDDDI_FILTER
product: Windows
targetos: Windows
req.typenames: DXVAHDDDI_FILTER
---

# _DXVAHDDDI_FILTER enumeration


## -description


The DXVAHDDDI_FILTER enumeration contains values that identify the filter range, which the driver should retrieve when the driver's <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_getcaps.md">GetCaps</a> function is called with the D3DDDICAPS_DXVAHD_GETVPFILTERRANGE value set. 


## -syntax


````
typedef enum _DXVAHDDDI_FILTER { 
  DXVAHDDDI_FILTER_BRIGHTNESS          = 0,
  DXVAHDDDI_FILTER_CONTRAST            = 1,
  DXVAHDDDI_FILTER_HUE                 = 2,
  DXVAHDDDI_FILTER_SATURATION          = 3,
  DXVAHDDDI_FILTER_NOISE_REDUCTION     = 4,
  DXVAHDDDI_FILTER_EDGE_ENHANCEMENT    = 5,
  DXVAHDDDI_FILTER_ANAMORPHIC_SCALING  = 6
} DXVAHDDDI_FILTER;
````


## -enum-fields




### -field DXVAHDDDI_FILTER_BRIGHTNESS

A value that specifies the filter range of the brightness ProcAmp. 


### -field DXVAHDDDI_FILTER_CONTRAST

A value that specifies the filter range of the contrast ProcAmp. 


### -field DXVAHDDDI_FILTER_HUE

A value that specifies the filter range of the hue ProcAmp. 


### -field DXVAHDDDI_FILTER_SATURATION

A value that specifies the filter range of the saturation ProcAmp. 


### -field DXVAHDDDI_FILTER_NOISE_REDUCTION

A value that specifies the filter range of the noise reduction filter. 


### -field DXVAHDDDI_FILTER_EDGE_ENHANCEMENT

A value that specifies the filter range of the edge enhancement filter. 


### -field DXVAHDDDI_FILTER_ANAMORPHIC_SCALING

A value that specifies that the filter range of anamorphic scaling. 


## -see-also

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_getcaps.md">GetCaps</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXVAHDDDI_FILTER enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

