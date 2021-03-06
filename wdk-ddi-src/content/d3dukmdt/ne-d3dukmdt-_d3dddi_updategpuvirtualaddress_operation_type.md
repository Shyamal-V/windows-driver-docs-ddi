---
UID: NE:d3dukmdt._D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE
title: "_D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE"
author: windows-driver-content
description: D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE describes the details of the virtual address update operation being performed.
old-location: display\d3dddi_updategpuvirtualaddress_operation_type.htm
old-project: display
ms.assetid: 47B53DDA-E04B-4DA5-BEAB-8515B6683AE4
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP_PROTECT, D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE, d3dukmdt/D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP, d3dukmdt/D3DDDI_UPDATEGPUVIRTUALADDRESS_UNMAP, D3DDDI_UPDATEGPUVIRTUALADDRESS_UNMAP, D3DDDI_UPDATEGPUVIRTUALADDRESS_COPY, _D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE, d3dukmdt/D3DDDI_UPDATEGPUVIRTUALADDRESS_COPY, display.d3dddi_updategpuvirtualaddress_operation_type, d3dukmdt/D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP_PROTECT, d3dukmdt/D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE, D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE enumeration [Display Devices], D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dukmdt.h
req.include-header: D3dumddi.h, D3dkmddi.h
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
-	HeaderDef
apilocation:
-	d3dukmdt.h
apiname:
-	D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE
product: Windows
targetos: Windows
req.typenames: D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE
---

# _D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE enumeration


## -description


<b>D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE</b> describes the  details of the virtual address update operation being performed.
  


## -syntax


````
typedef enum _D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE { 
  D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP          = 0,
  D3DDDI_UPDATEGPUVIRTUALADDRESS_UNMAP        = 1,
  D3DDDI_UPDATEGPUVIRTUALADDRESS_COPY         = 2,
  D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP_PROTECT  = 3
} D3DDDI_UPDATEGPUVIRTUALADDRESS_OPERATION_TYPE;
````


## -enum-fields




### -field D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP

Maps the given virtual address range to the given allocation range. The allocation does not have to be resident at the time of submission or at the time of mapping. The read-write protection is set to the pages. <b>DriverProtection</b> for the pages is set to zero.


### -field D3DDDI_UPDATEGPUVIRTUALADDRESS_UNMAP

Puts the specified virtual address range to the <i>zero</i> state or to the <i>invalid</i> state.


### -field D3DDDI_UPDATEGPUVIRTUALADDRESS_COPY

The <i>copy</i> operation copies all mappings from source GPU virtual address range to the destination range. The source and destination ranges are allowed to intersect. Both ranges must belong to a reserved (zero) virtual address range.


### -field D3DDDI_UPDATEGPUVIRTUALADDRESS_MAP_PROTECT

Maps the given virtual address range to the given allocation range. The allocation does not have to be resident at the time of submission or at the time of mapping. The page protection is specified in the operation.

