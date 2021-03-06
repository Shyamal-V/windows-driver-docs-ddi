---
UID: NN:wdtf.IWDTFTarget2
title: IWDTFTarget2
author: windows-driver-content
description: Defines operations and properties for a testable item.
old-location: dtf\iwdtftarget2.htm
old-project: dtf
ms.assetid: fc75c201-a3ff-44f7-ba09-8e3554b1cf27
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: dtf.iwdtftarget2, IWDTFTarget2 interface [Windows Device Testing Framework], IWDTFTarget2 interface [Windows Device Testing Framework], described, IWDTFTarget2, wdtf/IWDTFTarget2, Microsoft.WDTF.IWDTFTarget2
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
-	IWDTFTarget2
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFTarget2 interface


## -description


Defines operations and properties for a testable item.


## -members

The <b>IWDTFTarget2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439396">Eval</a>
</td>
<td align="left" width="63%">
Evaluates whether this target matches an SDEL statement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439398">GetInterface</a>
</td>
<td align="left" width="63%">
Returns an action for the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439400">GetRelations</a>
</td>
<td align="left" width="63%">
Returns a collection of related targets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Returns a value from the target that is associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439407">GetValueBool</a>
</td>
<td align="left" width="63%">
Returns a boolean value from the target that is associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439410">GetValueLongNumber</a>
</td>
<td align="left" width="63%">
Returns a long number value from the target that is associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439416">GetValueLongNumbers</a>
</td>
<td align="left" width="63%">
Returns a collection of long number values from the target that are associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439421">GetValueNumber</a>
</td>
<td align="left" width="63%">
Returns a number value from the target that is associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439426">GetValueNumbers</a>
</td>
<td align="left" width="63%">
Returns a collection of number values from the target that are associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439431">GetValueString</a>
</td>
<td align="left" width="63%">
Returns a string value from the target that is associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439437">GetValueStrings</a>
</td>
<td align="left" width="63%">
Returns a collection of string values from the target that are associated with a specified attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439441">HasContext</a>
</td>
<td align="left" width="63%">
Determines whether a given context exists for the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439447">HasInterface</a>
</td>
<td align="left" width="63%">
Determines whether the target supports a given interface.

</td>
</tr>
</table>Evaluates whether this target matches an SDEL statement.

Returns an action for the target.

Returns a collection of related targets.

Returns a value from the target that is associated with a specified attribute.

Returns a boolean value from the target that is associated with a specified attribute.

Returns a long number value from the target that is associated with a specified attribute.

Returns a collection of long number values from the target that are associated with a specified attribute.

Returns a number value from the target that is associated with a specified attribute.

Returns a collection of number values from the target that are associated with a specified attribute.

Returns a string value from the target that is associated with a specified attribute.

Returns a collection of string values from the target that are associated with a specified attribute.

Determines whether a given context exists for the target.

Determines whether the target supports a given interface.

 

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWDTFTarget2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="..\ntddk\ns-ntddk-_context.md">Context</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a name-value pair that represents user data for the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that identifies the depot that the target comes from.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406421">WDTF</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the main WDTF aggregation object.

</td>
</tr>
</table>
<a href="..\ntddk\ns-ntddk-_context.md">Context</a>


Read/write

Gets and sets a name-value pair that represents user data for the target.


<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


Read-only

Gets a value that identifies the depot that the target comes from.


<a href="https://msdn.microsoft.com/library/windows/hardware/hh406421">WDTF</a>


Read-only

Gets the main WDTF aggregation object.

 


## -remarks



The <b>IWDTFTarget2</b> interface abstracts the notion of a testable item, 
which is the central focus of the WDTF object model.
You can retrieve instances of the <b>IWDTFTarget2</b> interface only 
through other interfaces (such as the 
<a href="..\wdtf\nn-wdtf-iwdtfdevicedepot2.md">IWDTFDeviceDepot2</a> interface or
the <a href="..\wdtf\nn-wdtf-iwdtfsystemdepot2.md">IWDTFSystemDepot2</a> interface). 

The lifetime of a target is tied to its creator; that is, if you retrieve a target 
from the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406304">DeviceDepot</a> property, 
the target will exist as long as the <b>DeviceDepot</b> 
property exists.

You cannot copy an instance of the <b>IWDTFTarget2</b> interface. 
Even if you add a target to a collection, you really just add a reference to the same instance.

<b>Implementation Details</b>

ProgID: (Use the <a href="https://msdn.microsoft.com/3034f790-471f-46c2-915a-15074ae72960">IWDTF</a> 
aggregation interface to instantiate)

TraceLevel Path: HKCR\WDTF.Target.1\

<div class="alert"><b>Note</b>  The implementation of this interface is not thread-safe.</div>
<div> </div>


