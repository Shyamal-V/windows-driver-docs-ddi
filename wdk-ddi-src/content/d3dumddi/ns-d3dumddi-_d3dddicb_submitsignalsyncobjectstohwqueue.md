---
UID: NS:d3dumddi._D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE
title: "_D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE"
author: windows-driver-content
description: A structure that holds information to submit a signal synchronization object to a hardware queue.
old-location: display\d3dddicb_submitsignalsyncobjectstohwqueue.htm
old-project: display
ms.assetid: 22AA35D4-D287-443B-A49D-87C20BD436AA
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.d3dddicb_submitsignalsyncobjectstohwqueue, _D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE, D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE, D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE structure [Display Devices], d3dumddi/D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dumddi.h
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
-	d3dumddi.h
apiname:
-	D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE
product: Windows
targetos: Windows
req.typenames: D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE
---

# _D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE structure


## -description


A structure that holds information to submit a signal synchronization object to a hardware queue.


## -syntax


````
typedef struct _D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE {
  D3DDDICB_SIGNALFLAGS     Flags;
  ULONG                    BroadcastHwQueueCount;
  const HANDLE             *BroadcastHwQueueArray;
  UINT                     ObjectCount;
  const D3DKMT_HANDLE      *ObjectHandleArray;
  const UINT64             *FenceValueArray;
} D3DDDICB_SUBMITSIGNALSYNCOBJECTSTOHWQUEUE;
````


## -struct-fields




### -field Flags

Specifies signal behavior.


### -field BroadcastHwQueueCount

Specifies the number of hardware queues to broadcast this signal to.


### -field BroadcastHwQueueArray

Specifies hardware queue handles to broadcast to.



### -field ObjectCount

Number of objects to signal.



### -field ObjectHandleArray

Handles to monitored fence synchronization objects to signal.


### -field FenceValueArray

monitored fence values to signal.


