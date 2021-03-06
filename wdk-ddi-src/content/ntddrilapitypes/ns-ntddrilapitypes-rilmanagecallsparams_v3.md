---
UID: NS:ntddrilapitypes.RILMANAGECALLSPARAMS_V3
title: RILMANAGECALLSPARAMS_V3
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilmanagecallsparams_v3.htm
old-project: netvista
ms.assetid: a398086b-827e-4684-a79c-db849926b3c3
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.rilmanagecallsparams_v3, RILMANAGECALLSPARAMS_V3 structure [Network Drivers Starting with Windows Vista], ntddrilapitypes/RILMANAGECALLSPARAMS_V3, RILMANAGECALLSPARAMS_V3, *LPRILMANAGECALLSPARAMS_V3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddrilapitypes.h
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
-	ntddrilapitypes.h
apiname:
-	RILMANAGECALLSPARAMS_V3
product: Windows
targetos: Windows
req.typenames: RILMANAGECALLSPARAMS_V3, *LPRILMANAGECALLSPARAMS_V3
---

# RILMANAGECALLSPARAMS_V3 structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILMANAGECALLSPARAMS_V3 {
  DWORD                       dwExecutor;
  RILMANAGECALLPARAMSCOMMAND  dwCommand;
  DWORD                       dwID;
  BOOL                        fHasOfferAnswer;
  RILCALLMEDIAOFFERANSWERSET  rcmOfferAnswer;
  RILADDRESS                  raAddress;
} RILMANAGECALLSPARAMS_V3, RILMANAGECALLSPARAMS_V3;
````


## -struct-fields




### -field dwExecutor


### -field dwCommand


### -field dwID


### -field fHasOfferAnswer


### -field rcmOfferAnswer


### -field raAddress

