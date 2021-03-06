---
UID: NE:d3dkmddi._DXGK_PATH_UPDATE
title: "_DXGK_PATH_UPDATE"
author: windows-driver-content
description: Enum which indicates how this path has been modified since the previous successful call to SetTimingsFromVidPn.
old-location: display\dxgk_path_update.htm
old-project: display
ms.assetid: DCBBFBF7-73B2-4298-BB87-83E1C6D76BD0
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: DXGK_PATH_UPDATE, d3dkmddi/DXGK_PATH_UPDATE_ADDED, DXGK_PATH_UPDATE_ADDED, _DXGK_PATH_UPDATE, display.dxgk_path_update, DXGK_PATH_UPDATE_UNMODIFED, DXGK_PATH_UPDATE_REMOVED, d3dkmddi/DXGK_PATH_UPDATE_REMOVED, DXGK_PATH_UPDATE enumeration [Display Devices], d3dkmddi/DXGK_PATH_UPDATE_MODIFIED, d3dkmddi/DXGK_PATH_UPDATE, DXGK_PATH_UPDATE_MODIFIED, d3dkmddi/DXGK_PATH_UPDATE_UNMODIFED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dkmddi.h
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
req.irql: PASSIVE_LEVEL
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	d3dkmddi.h
apiname:
-	DXGK_PATH_UPDATE
product: Windows
targetos: Windows
req.typenames: DXGK_PATH_UPDATE
---

# _DXGK_PATH_UPDATE enumeration


## -description


Enum which indicates how this path has been modified since the previous successful call to SetTimingsFromVidPn.


## -syntax


````
typedef enum _DXGK_PATH_UPDATE { 
  DXGK_PATH_UPDATE_UNMODIFED  = 0,
  DXGK_PATH_UPDATE_ADDED      = 1,
  DXGK_PATH_UPDATE_MODIFIED   = 2,
  DXGK_PATH_UPDATE_REMOVED    = 3
} DXGK_PATH_UPDATE;
````


## -enum-fields




### -field DXGK_PATH_UPDATE_UNMODIFIED


### -field DXGK_PATH_UPDATE_ADDED

Indicates that this path is new so the driver will have to fully comprehend the description of what is required.  Since there is no allocation from which to scan out, the driver must scan out black until the OS associates one or more planes to be scanned out.


### -field DXGK_PATH_UPDATE_MODIFIED

Indicates that this path has been changed since the last call to SetTimingsFromVidPn.  The driver will have to interrogate the VidPn and check the other path info fields in order to understand what has changed.  The OS will have removed all pixel planes prior to making this call so the driver must scan out black until the OS associates one or more planes to be scanned out.




### -field DXGK_PATH_UPDATE_REMOVED

Indicates that this path was present in the previous VidPn but has been removed. The driver should be able to optimize the removal without interrogating VidPn to see that the path has been removed. 


### -field UINT




#### - DXGK_PATH_UPDATE_UNMODIFED

Indicates that this path has not been changed since the last call to SetTimingsFromVidPn.  This allows the driver to skip interrogating VidPn for changes.  Existing scan-out should continue, other than any glitching which might be caused due to reassignment of display resources to satisfy other paths.

