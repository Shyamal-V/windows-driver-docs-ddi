---
UID: NC:ucxroothub.EVT_UCX_ROOTHUB_INTERRUPT_TX
title: EVT_UCX_ROOTHUB_INTERRUPT_TX
author: windows-driver-content
description: The client driver's implementation that UCX calls when it receives a request for information about changed ports.
old-location: buses\evt_ucx_roothub_interrupt_tx.htm
old-project: usbref
ms.assetid: e2371b90-2274-459b-9e4a-5c9936d21b9c
ms.author: windowsdriverdev
ms.date: 2/8/2018
ms.keywords: buses.evt_ucx_roothub_interrupt_tx, EvtUcxInterruptTransferTx callback function [Buses], EvtUcxInterruptTransferTx, EVT_UCX_ROOTHUB_INTERRUPT_TX, EVT_UCX_ROOTHUB_INTERRUPT_TX, ucxroothub/EvtUcxInterruptTransferTx, PEVT_UCX_ROOTHUB_INTERRUPT_TX callback function pointer [Buses], PEVT_UCX_ROOTHUB_INTERRUPT_TX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ucxroothub.h
req.include-header: Ucxclass.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: DISPATCH_LEVEL
topictype:
-	APIRef
-	kbSyntax
apitype:
-	UserDefined
apilocation:
-	ucxroothub.h
apiname:
-	PEVT_UCX_ROOTHUB_INTERRUPT_TX
product: Windows
targetos: Windows
req.typenames: UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, *PUCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS
req.product: Windows 10 or later.
---

# EVT_UCX_ROOTHUB_INTERRUPT_TX callback


## -description


The client driver's implementation that UCX calls when it receives a request for information about changed ports.


## -prototype


````
EVT_UCX_ROOTHUB_INTERRUPT_TX EvtUcxInterruptTransferTx;

VOID EvtUcxInterruptTransferTx(
  _In_ UCXROOTHUB UcxRootHub,
  _In_ WDFREQUEST Request
)
{ ... }

typedef EVT_UCX_ROOTHUB_INTERRUPT_TX PEVT_UCX_ROOTHUB_INTERRUPT_TX;
````


## -parameters




### -param UcxRootHub [in]

A handle to a UCX object that represents the root hub.


### -param Request [in]

Contains the <a href="..\usb\ns-usb-_urb.md">URB</a> for the root hub interrupt transfer request.


## -returns



This callback function does not return a value.




## -remarks



The UCX client driver registers this callback function with the USB host controller extension (UCX) by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/mt188048">UcxRootHubCreate</a>
 method.

 The <i>Request</i> parameter contains a buffer in which each bit corresponds to a root
    hub port, with the first bit corresponding to the first port.  The
    client driver sets the corresponding bit if any port has changed, and then completes the request.

The client driver returns completion status in <i>Request</i>.


#### Examples

This snippet shows how the callback extracts the root hub interrupt transfer request.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>        WDF_REQUEST_PARAMETERS_INIT(&amp;wdfRequestParams);
        WdfRequestGetParameters(WdfRequest, &amp;wdfRequestParams);

        urb = (PURB)wdfRequestParams.Parameters.Others.Arg1;
        transferBuffer = urb-&gt;UrbBulkOrInterruptTransfer.TransferBuffer;
        transferBufferLength = urb-&gt;UrbBulkOrInterruptTransfer.TransferBufferLength;
</pre>
</td>
</tr>
</table></span></div>


