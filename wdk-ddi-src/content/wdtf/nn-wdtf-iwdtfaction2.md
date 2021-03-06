---
UID: NN:wdtf.IWDTFAction2
title: IWDTFAction2
author: windows-driver-content
description: Defines operations and properties that can control an instance of the IWDTFTarget2 interface.
old-location: dtf\iwdtfaction2.htm
old-project: dtf
ms.assetid: 0ca56301-9e46-4082-a5a4-41a9c655fbd8
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: dtf.iwdtfaction2, IWDTFAction2 interface [Windows Device Testing Framework], IWDTFAction2 interface [Windows Device Testing Framework], described, IWDTFAction2, wdtf/IWDTFAction2, Microsoft.WDTF.IWDTFAction2
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
-	IWDTFAction2
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFAction2 interface


## -description


Defines operations and properties that can control an instance of the 
<a href="..\wdtf\nn-wdtf-iwdtftarget2.md">IWDTFTarget2</a> interface.


## -members

The <b>IWDTFAction2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406383">DisableObjectErrorLogging</a>
</td>
<td align="left" width="63%">
Disables object error logging for the action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406315">DisableObjectLogging</a>
</td>
<td align="left" width="63%">
Disables object logging for the action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406317">EnableObjectErrorLogging</a>
</td>
<td align="left" width="63%">
Enables object error logging for the action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406319">EnableObjectLogging</a>
</td>
<td align="left" width="63%">
Enables object logging for the action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Returns the status code for the last operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406323">GetStatusString</a>
</td>
<td align="left" width="63%">
Returns the status for the last operation as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406325">IsStatusSuccess</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the last operation was successful.

</td>
</tr>
</table>Disables object error logging for the action.

Disables object logging for the action.

Enables object error logging for the action.

Enables object logging for the action.

Returns the status code for the last operation.

Returns the status for the last operation as a string.

Gets a value that indicates whether the last operation was successful.

 

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWDTFAction2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406329">Target</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the target to which this action refers.

</td>
</tr>
</table>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406329">Target</a>


Read-only

Gets the target to which this action refers.

 

