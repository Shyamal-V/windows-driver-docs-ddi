---
UID: NN:wdtf.IWDTFNumbers2
title: IWDTFNumbers2
author: windows-driver-content
description: Defines operations and properties for a collection of numbers.
old-location: dtf\iwdtfnumbers2.htm
old-project: dtf
ms.assetid: 8cff3bc3-771f-47b7-bf4b-b7221f498252
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: dtf.iwdtfnumbers2, IWDTFNumbers2 interface [Windows Device Testing Framework], IWDTFNumbers2 interface [Windows Device Testing Framework], described, IWDTFNumbers2, wdtf/IWDTFNumbers2, Microsoft.WDTF.IWDTFNumbers2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wdtf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTF.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTF.Interop.metadata_dll
req.type-library: 
req.lib: wdtf.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTF.Interop.metadata_dll.dll
apiname:
-	IWDTFNumbers2
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFNumbers2 interface


## -description


Defines operations and properties for a collection of numbers.


## -members

The <b>IWDTFNumbers2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a single number to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes a number from the collection.

</td>
</tr>
</table>Adds a single number to the collection.

Removes a number from the collection.

 

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWDTFNumbers2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a new iteration variable that the <b>For Each</b> 
loop structure implicitly uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of numbers in this collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an individual number in the collection.

</td>
</tr>
</table>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


Read-only

Gets a new iteration variable that the <b>For Each</b> 
loop structure implicitly uses.


<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


Read-only

Gets the number of numbers in this collection.


<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


Read-only

Gets an individual number in the collection.

 

