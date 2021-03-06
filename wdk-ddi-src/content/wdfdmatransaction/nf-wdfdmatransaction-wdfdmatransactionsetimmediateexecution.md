---
UID: NF:wdfdmatransaction.WdfDmaTransactionSetImmediateExecution
title: WdfDmaTransactionSetImmediateExecution function
author: windows-driver-content
description: The WdfDmaTransactionSetImmediateExecution method marks the specified DMA transaction so that calls to WdfDmaTransactionExecute and WdfDmaTransactionAllocateResources initiate the transaction immediately or fail.
old-location: wdf\wdfdmatransactionsetimmediateexecution.htm
old-project: wdf
ms.assetid: BC260058-1E33-43BA-B75E-79540E36A08D
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: kmdf.wdfdmatransactionsetimmediateexecution, PFN_WDFDMATRANSACTIONSETIMMEDIATEEXECUTION, wdf.wdfdmatransactionsetimmediateexecution, wdfdmatransaction/WdfDmaTransactionSetImmediateExecution, WdfDmaTransactionSetImmediateExecution method, WdfDmaTransactionSetImmediateExecution
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfdmatransaction.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: 
req.kmdf-ver: 1.11
req.umdf-ver: 
req.ddi-compliance: DriverCreate
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (see Framework Library Versioning.)
req.dll: 
req.irql: "<=DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	LibDef
apilocation:
-	Wdf01000.sys
-	Wdf01000.sys.dll
apiname:
-	WdfDmaTransactionSetImmediateExecution
product: Windows
targetos: Windows
req.typenames: "*PWDF_DMA_SYSTEM_PROFILE_CONFIG, WDF_DMA_SYSTEM_PROFILE_CONFIG"
req.product: Windows 10 or later.
---

# WdfDmaTransactionSetImmediateExecution function


## -description


<p class="CCE_Message">[Applies to KMDF only]

The <b>WdfDmaTransactionSetImmediateExecution</b> method
   marks the specified DMA transaction so  that calls to <a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionexecute.md">WdfDmaTransactionExecute</a>  and <a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionallocateresources.md">WdfDmaTransactionAllocateResources</a> initiate the transaction immediately or fail.


## -syntax


````
void WdfDmaTransactionSetImmediateExecution(
  _In_ WDFDMATRANSACTION DmaTransaction,
  _In_ BOOLEAN           UseImmediateExecution
);
````


## -parameters




### -param DmaTransaction [in]

A handle to a DMA transaction object to mark for immediate execution.


### -param UseImmediateExecution [in]

A Boolean value which, if TRUE, indicates that the transaction should execute immediately (or fail if resources are not available), and, if FALSE, indicates that the transaction should be queued for execution once DMA resources are available.


## -returns



This method does not return a value.




## -remarks



Before calling <b>WdfDmaTransactionSetImmediateExecution</b>, the driver must initialize the transaction.

If the driver calls <a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionexecute.md">WdfDmaTransactionExecute</a>  or <a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionallocateresources.md">WdfDmaTransactionAllocateResources</a> after calling <b>WdfDmaTransactionSetImmediateExecution</b> with <i>UseImmediateExecution</i> set to TRUE, and the resources needed for the request are unavailable, that method returns STATUS_INSUFFICIENT_RESOURCES. If the required resources are available, the framework claims them and initiates the call synchronously.

After the driver marks a transaction for immediate execution, the transaction remains marked as such until the driver calls <a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionrelease.md">WdfDmaTransactionRelease</a> or clears the flag by calling <b>WdfDmaTransactionSetImmediateExecution</b> with <i>UseImmediateExecution</i> set to FALSE.

<b>WdfDmaTransactionSetImmediateExecution</b> requires DMA version 3.
 To select DMA version 3, set the <b>WdmDmaVersionOverride</b> member of <a href="..\wdfdmaenabler\ns-wdfdmaenabler-_wdf_dma_enabler_config.md">WDF_DMA_ENABLER_CONFIG</a> to 3.

If your driver calls this method on an operating system earlier than Windows 8, <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-kmdf-verifier">the framework's verifier</a> reports an error.




## -see-also

<a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionexecute.md">WdfDmaTransactionExecute</a>



<a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionrelease.md">WdfDmaTransactionRelease</a>



<a href="..\wdfdmatransaction\nf-wdfdmatransaction-wdfdmatransactionallocateresources.md">WdfDmaTransactionAllocateResources</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WdfDmaTransactionSetImmediateExecution method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

