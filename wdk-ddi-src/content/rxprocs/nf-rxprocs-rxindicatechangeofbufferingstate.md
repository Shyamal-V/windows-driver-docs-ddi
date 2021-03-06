---
UID: NF:rxprocs.RxIndicateChangeOfBufferingState
title: RxIndicateChangeOfBufferingState function
author: windows-driver-content
description: RxIndicateChangeOfBufferingState is called to register a change buffering state request (an oplock break indication, for example) for later processing. If necessary, worker thread routines for further processing are activated.
old-location: ifsk\rxindicatechangeofbufferingstate.htm
old-project: ifsk
ms.assetid: 981f5a33-a4f1-438c-8fcf-03a5ab4c0e44
ms.author: windowsdriverdev
ms.date: 2/7/2018
ms.keywords: rxref_4a7ba539-c0b8-4c3b-b642-c272d262310b.xml, rxprocs/RxIndicateChangeOfBufferingState, RxIndicateChangeOfBufferingState routine [Installable File System Drivers], ifsk.rxindicatechangeofbufferingstate, RxIndicateChangeOfBufferingState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rxprocs.h
req.include-header: Rxprocs.h, Struchdr.h, Fcb.h
req.target-type: Desktop
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
req.irql: "<= APC_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	rxprocs.h
apiname:
-	RxIndicateChangeOfBufferingState
product: Windows
targetos: Windows
req.typenames: RX_CONTEXT, *PRX_CONTEXT
req.product: Windows 10 or later.
---

# RxIndicateChangeOfBufferingState function


## -description


<b>RxIndicateChangeOfBufferingState</b> is called to register a change buffering state request (an oplock break indication, for example) for later processing. If necessary, worker thread routines for further processing are activated.


## -syntax


````
VOID RxIndicateChangeOfBufferingState(
   PMRX_SRV_CALL SrvCall,
   PVOID         SrvOpenKey,
   PVOID         MRxContext
);
````


## -parameters




### -param SrvCall

A pointer to the SRV_CALL structure.


### -param SrvOpenKey

A pointer to the key for the SRV_OPEN structure.


### -param Context

TBD




#### - MRxContext

A pointer to the context to be passed back to the network mini-redirector during callbacks for processing the request.


## -returns



None




## -remarks



<b>RxIndicateChangeOfBufferingState</b> registers the change buffering state request by either inserting it in the registration list (DPC Level processing ) or the appropriate dispatcher/handler list.

This is an instance in which the buffering state change request from the server identifies the SRV_OPEN structure using the key generated by the server. This implies that the key needs to be mapped onto the SRV_OPEN structure locally.

The internal routines called by this routine can fail because of a lack of available memory (unable to allocate non-paged pool memory, for example), but since this is a VOID routine no error is returned when this condition occurs.

If a buffering state request can be processed immediately instead of being queued for processing later, then <b>RxChangeBufferingState</b> can be called. 




## -see-also

<a href="..\rxprocs\nf-rxprocs-rxchangebufferingstate.md">RxChangeBufferingState</a>



<a href="https://msdn.microsoft.com/6cf4c6f6-a21f-4919-92b5-2403b650d8d0">The SRV_OPEN Structure</a>



<a href="..\rxprocs\nf-rxprocs-rxindicatechangeofbufferingstateforsrvopen.md">RxIndicateChangeOfBufferingStateForSrvOpen</a>



<a href="..\rxcontx\ns-rxcontx-_rx_context.md">RX_CONTEXT</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RxIndicateChangeOfBufferingState routine%20 RELEASE:%20(2/7/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

