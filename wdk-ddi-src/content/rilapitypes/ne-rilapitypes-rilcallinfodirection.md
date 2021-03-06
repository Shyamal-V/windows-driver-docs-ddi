---
UID: NE:rilapitypes.RILCALLINFODIRECTION
title: RILCALLINFODIRECTION
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcallinfodirection_2.htm
old-project: netvista
ms.assetid: 55db88f4-14a5-4d37-b4e8-be88369f33b7
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: rilapitypes/RIL_CALLDIR_MAX, RIL_CALLDIR_MAX, RILCALLINFODIRECTION enumeration [Network Drivers Starting with Windows Vista], rilapitypes/RILCALLINFODIRECTION, netvista.rilcallinfodirection_2, RILCALLINFODIRECTION, rilapitypes/RIL_CALLDIR_OUTGOING, RIL_CALLDIR_OUTGOING
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: rilapitypes.h
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	rilapitypes.h
apiname:
-	RILCALLINFODIRECTION
product: Windows
targetos: Windows
req.typenames: RILCALLINFODIRECTION
req.product: Windows 10 or later.
---

# RILCALLINFODIRECTION enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef enum _RILCALLINFODIRECTION { 
  RIL_CALLDIR_OUTGOING,
  RIL_CALLDIR_MAX
} RILCALLINFODIRECTION;
````


## -enum-fields




### -field RIL_CALLDIR_INCOMING


### -field RIL_CALLDIR_OUTGOING


### -field RIL_CALLDIR_MAX

