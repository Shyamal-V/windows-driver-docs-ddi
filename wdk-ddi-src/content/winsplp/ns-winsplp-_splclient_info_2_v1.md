---
UID: NS:winsplp._SPLCLIENT_INFO_2_V1
title: "_SPLCLIENT_INFO_2_V1"
author: windows-driver-content
description: Contains the handle for the server-side printer that is used to make direct API calls from the client to the server without the overhead of the RPC.
old-location: print\splclient_info_2_w2k.htm
old-project: print
ms.assetid: 713246FE-355B-4C01-A8DF-535BDBA0FCB8
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: winsplp/SPLCLIENT_INFO_2_W2K, _SPLCLIENT_INFO_2_V1, print.splclient_info_2_w2k, SPLCLIENT_INFO_2_W2K, SPLCLIENT_INFO_2_W2K structure [Print Devices], *LPSPLCLIENT_INFO_2, SPLCLIENT_INFO_2, *PSPLCLIENT_INFO_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsplp.h
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
-	Winsplp.h
apiname:
-	SPLCLIENT_INFO_2_W2K
product: Windows
targetos: Windows
req.typenames: SPLCLIENT_INFO_2_W2K
req.product: Windows 10 or later.
---

# _SPLCLIENT_INFO_2_V1 structure


## -description


Contains the handle for the server-side printer that is used to make direct API calls from the client to the server without the overhead of the RPC. The performance improvement is primarily observed in calls to read/write printer made from within the spooler (Gdi32.dll during playback). This structure is used in the private spooler RPC interface (RpcSplOpenPrinter).


## -syntax


````
typedef struct _SPLCLIENT_INFO_2_V1 {
  ULONG_PTR        hSplPrinter;
} SPLCLIENT_INFO_2_W2K;
````


## -struct-fields




### -field hSplPrinter

Specifies the server-side handle to be used for direct calls.

