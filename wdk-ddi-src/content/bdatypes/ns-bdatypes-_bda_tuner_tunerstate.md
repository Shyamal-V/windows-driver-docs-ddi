---
UID: NS:bdatypes._BDA_TUNER_TUNERSTATE
title: "_BDA_TUNER_TUNERSTATE"
author: windows-driver-content
description: "."
old-location: stream\bda_tuner_tunerstate.htm
old-project: stream
ms.assetid: 77B30ADC-27F2-4883-97FC-F6C29B539EE0
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: stream.bda_tuner_tunerstate, PBDA_TUNER_TUNERSTATE structure pointer [Streaming Media Devices], bdatypes/PBDA_TUNER_TUNERSTATE, _BDA_TUNER_TUNERSTATE, *PBDA_TUNER_TUNERSTATE, BDA_TUNER_TUNERSTATE, bdatypes/BDA_TUNER_TUNERSTATE, BDA_TUNER_TUNERSTATE structure [Streaming Media Devices], PBDA_TUNER_TUNERSTATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
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
-	Bdatypes.h
apiname:
-	BDA_TUNER_TUNERSTATE
product: Windows
targetos: Windows
req.typenames: "*PBDA_TUNER_TUNERSTATE, BDA_TUNER_TUNERSTATE"
---

# _BDA_TUNER_TUNERSTATE structure


## -description





## -syntax


````
typedef struct _BDA_TUNER_TUNERSTATE {
  PBDARESULT lResult;
  ULONG      ulTuneLength;
  BYTE       argbTuneData[MIN_DIMENSION];
} BDA_TUNER_TUNERSTATE, *PBDA_TUNER_TUNERSTATE;
````


## -struct-fields




### -field lResult


### -field ulTuneLength


### -field argbTuneData

