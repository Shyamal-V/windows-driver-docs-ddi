---
UID: NF:rilapi.RIL_GetCardInfo
title: RIL_GetCardInfo function
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\ril_getcardinfo.htm
old-project: netvista
ms.assetid: d865993b-10cc-4fa2-a00f-34eb1d4e299b
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.ril_getcardinfo, RIL_GetCardInfo method [Network Drivers Starting with Windows Vista], rilapi/RIL_GetCardInfo, RIL_GetCardInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rilapi.h
req.include-header: 
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	rilapi.h
apiname:
-	RIL_GetCardInfo
product: Windows
targetos: Windows
req.typenames: RH_QUERY_CONNECTION_PROPERTIES_OUTPUT_BUFFER, *PRH_QUERY_CONNECTION_PROPERTIES_OUTPUT_BUFFER
req.product: Windows 10 or later.
---

# RIL_GetCardInfo function


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 

            


## -syntax


````
HRESULT  RIL_GetCardInfo(
   HRIL   hRil,
   LPVOID lpContext,
   DWORD  dwSlotIndex
);
````


## -parameters




### -param hRil


### -param lpContext


### -param dwSlotIndex


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



