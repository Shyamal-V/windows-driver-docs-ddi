---
UID: NN:printerextension.IPrinterExtensionAsyncOperation
title: IPrinterExtensionAsyncOperation
author: windows-driver-content
description: Provides the context associated with an asynchronous operation.
old-location: print\iprinterextensionasyncoperation.htm
old-project: print
ms.assetid: AA862667-42D6-4A82-9698-1C43E9EEC434
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: print.iprinterextensionasyncoperation, IPrinterExtensionAsyncOperation interface [Print Devices], IPrinterExtensionAsyncOperation interface [Print Devices], described, IPrinterExtensionAsyncOperation, printerextension/IPrinterExtensionAsyncOperation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: printerextension.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	Printerextension.h
apiname:
-	IPrinterExtensionAsyncOperation
product: Windows
targetos: Windows
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrinterExtensionAsyncOperation interface


## -description


Provides the context associated with an asynchronous operation.


## -members

The <b>IPrinterExtensionAsyncOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the asynchronous operation.

</td>
</tr>
</table>Cancels the asynchronous operation.

 


## -remarks



<b>IPrinterExtensionAsyncOperation</b> also helps to make it possible to perform device maintenance from a UWP device app or from a printer extension. For more information, see <a href="https://msdn.microsoft.com/310E92A9-F751-4346-9B2D-0578A136AD20">Device Maintenance</a>.




## -see-also

<a href="https://msdn.microsoft.com/310E92A9-F751-4346-9B2D-0578A136AD20">Device Maintenance</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265391">SendBidiSetRequestAsync</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrinterExtensionAsyncOperation interface%20 RELEASE:%20(2/2/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

