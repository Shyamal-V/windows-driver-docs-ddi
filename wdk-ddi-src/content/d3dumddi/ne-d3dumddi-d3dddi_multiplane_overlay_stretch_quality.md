---
UID: NE:d3dumddi.D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY
title: D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY
author: windows-driver-content
description: Identifies filtering processes that the hardware should perform when it stretches or shrinks multiplane overlay data.
old-location: display\d3dddi_multiplane_overlay_stretch_quality.htm
old-project: display
ms.assetid: 531F541F-4F53-4FAC-A1B7-B51467F34833
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_BILINEAR, d3dumddi/D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_BILINEAR, d3dumddi/D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_HIGH, display.d3dddi_multiplane_overlay_stretch_quality, d3dumddi/D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY, D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_HIGH, D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY enumeration [Display Devices], D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY
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
-	D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY
product: Windows
targetos: Windows
req.typenames: D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY
---

# D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY enumeration


## -description


Identifies filtering processes that the hardware should perform when it stretches or shrinks multiplane overlay data.


## -syntax


````
typedef enum D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY { 
  D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_BILINEAR  = 0x1,
  D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_HIGH      = 0x2
} D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY;
````


## -enum-fields




### -field D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_BILINEAR

When the hardware stretches or shrinks the data, it should perform bilinear filtering. If the hardware lacks enough resources to perform bilinear shrinking, the user-mode display driver can use point sampling.


### -field D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY_HIGH

When the hardware stretches or shrinks the data, it should perform the highest quality filtering that it supports.

