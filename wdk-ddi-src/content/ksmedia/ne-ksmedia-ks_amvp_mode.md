---
UID: NE:ksmedia.KS_AMVP_MODE
title: KS_AMVP_MODE
author: windows-driver-content
description: The KS_AMVP_MODE enumeration defines video port display modes.
old-location: stream\ks_amvp_mode.htm
old-project: stream
ms.assetid: 9464a17a-fa09-46c5-a4a7-d5cbd58deebd
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: KS_AMVP_MODE_WEAVE, ksmedia/KS_AMVP_MODE_SKIPODD, ksmedia/KS_AMVP_MODE, KS_AMVP_MODE_BOBINTERLEAVED, ksmedia/KS_AMVP_MODE_WEAVE, ksmedia/KS_AMVP_MODE_BOBNONINTERLEAVED, ksmedia/KS_AMVP_MODE_SKIPEVEN, KS_AMVP_MODE_SKIPEVEN, vidcapstruct_64634d5e-72a6-4300-9fa9-e1d6859f0813.xml, ksmedia/KS_AMVP_MODE_BOBINTERLEAVED, KS_AMVP_MODE_BOBNONINTERLEAVED, KS_AMVP_MODE enumeration [Streaming Media Devices], KS_AMVP_MODE_SKIPODD, stream.ks_amvp_mode, KS_AMVP_MODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ksmedia.h
req.include-header: Ksmedia.h
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
-	ksmedia.h
apiname:
-	KS_AMVP_MODE
product: Windows
targetos: Windows
req.typenames: KS_AMVP_MODE
---

# KS_AMVP_MODE enumeration


## -description


The KS_AMVP_MODE enumeration defines video port display modes.


## -syntax


````
typedef enum  { 
  KS_AMVP_MODE_WEAVE              = 0,
  KS_AMVP_MODE_BOBINTERLEAVED     = 1,
  KS_AMVP_MODE_BOBNONINTERLEAVED  = 2,
  KS_AMVP_MODE_SKIPEVEN           = 3,
  KS_AMVP_MODE_SKIPODD            = 4
} KS_AMVP_MODE;
````


## -enum-fields




### -field KS_AMVP_MODE_WEAVE

Specifies the weave method to display interlaced video. In the weave mode, alternating fields are combined to form a single frame.


### -field KS_AMVP_MODE_BOBINTERLEAVED

Specifies the interleaved bob method to display video. In the interleaved bob mode, each field is displayed individually, and the gaps between fields are filled with interpolated values.


### -field KS_AMVP_MODE_BOBNONINTERLEAVED

Specifies the non-interleaved bob method to display video.


### -field KS_AMVP_MODE_SKIPEVEN

Specifies that even video fields should be skipped when displaying video.


### -field KS_AMVP_MODE_SKIPODD

Specifies that odd video fields should be skipped when displaying video.

