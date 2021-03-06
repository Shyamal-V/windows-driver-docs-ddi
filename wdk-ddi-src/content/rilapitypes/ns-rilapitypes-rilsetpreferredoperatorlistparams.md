---
UID: NS:rilapitypes.RILSETPREFERREDOPERATORLISTPARAMS
title: RILSETPREFERREDOPERATORLISTPARAMS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilsetpreferredoperatorlistparams_2.htm
old-project: netvista
ms.assetid: ff498364-f9ea-437f-904b-170ba0df7826
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: rilapitypes/RILSETPREFERREDOPERATORLISTPARAMS, netvista.rilsetpreferredoperatorlistparams_2, RILSETPREFERREDOPERATORLISTPARAMS structure [Network Drivers Starting with Windows Vista], *LPRILSETPREFERREDOPERATORLISTPARAMS, RILSETPREFERREDOPERATORLISTPARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
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
-	RILSETPREFERREDOPERATORLISTPARAMS
product: Windows
targetos: Windows
req.typenames: RILSETPREFERREDOPERATORLISTPARAMS, *LPRILSETPREFERREDOPERATORLISTPARAMS
req.product: Windows 10 or later.
---

# RILSETPREFERREDOPERATORLISTPARAMS structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef struct _RILSETPREFERREDOPERATORLISTPARAMS {
  HUICCAPP             hUiccApp;
  DWORD                dwPreferredListSize;
  RILOPERATORNAMES [1] PreferredList;
} RILSETPREFERREDOPERATORLISTPARAMS, RILSETPREFERREDOPERATORLISTPARAMS;
````


## -struct-fields




### -field hUiccApp


### -field dwPreferredListSize


### -field PreferredList

