---
UID: NS:ksmedia.KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER
title: KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER
author: windows-driver-content
description: This structure contains the header information for a per-frame settings item.
old-location: stream\kscamera_perframesetting_cap_item_header.htm
old-project: stream
ms.assetid: 6E68CACB-4E0E-41E4-BAB6-0B7ECEFA92F6
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: "*PKSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER, stream.kscamera_perframesetting_cap_item_header, PKSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER, KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER, ksmedia/KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER, KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER structure [Streaming Media Devices], ksmedia/PKSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER, PKSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER structure pointer [Streaming Media Devices]"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ksmedia.h
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
-	Ksmedia.h
apiname:
-	KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER
product: Windows
targetos: Windows
req.typenames: "*PKSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER, KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER"
---

# KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER structure


## -description


This structure contains the header information for a per-frame settings item.


## -syntax


````
typedef struct {
  ULONG     Size;
  ULONG     Type;
  ULONGLONG Flags;
} KSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER, *PKSCAMERA_PERFRAMESETTING_CAP_ITEM_HEADER;
````


## -struct-fields




### -field Size

The size of this header and the item payload that follows.


### -field Type

The <a href="..\ksmedia\ne-ksmedia-kscamera_perframesetting_item_type.md">KSCAMERA_PERFRAMESETTING_ITEM_TYPE</a>.


### -field Flags

This contains the supported capability flags.

