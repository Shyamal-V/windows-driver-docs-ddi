---
UID: NF:dbgeng.IDebugSystemObjects2.GetTotalNumberThreads
title: IDebugSystemObjects2::GetTotalNumberThreads method
author: windows-driver-content
description: The GetTotalNumberThreads method returns the total number of threads for all the processes in the current target, in addition to the largest number of threads in any process for the current target.
old-location: debugger\gettotalnumberthreads.htm
old-project: debugger
ms.assetid: dce67b78-a5e0-4664-b183-f462bcd773c8
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: GetTotalNumberThreads method [Windows Debugging], IDebugSystemObjects3 interface, IDebugSystemObjects2 interface [Windows Debugging], GetTotalNumberThreads method, GetTotalNumberThreads method [Windows Debugging], IDebugSystemObjects interface, IDebugSystemObjects::GetTotalNumberThreads, dbgeng/IDebugSystemObjects4::GetTotalNumberThreads, dbgeng/IDebugSystemObjects::GetTotalNumberThreads, IDebugSystemObjects3 interface [Windows Debugging], GetTotalNumberThreads method, GetTotalNumberThreads method [Windows Debugging], IDebugSystemObjects2 interface, GetTotalNumberThreads, GetTotalNumberThreads method [Windows Debugging], dbgeng/IDebugSystemObjects2::GetTotalNumberThreads, debugger.gettotalnumberthreads, IDebugSystemObjects, IDebugSystemObjects_fece8f3e-8d85-492a-b1f8-beadc398613e.xml, dbgeng/IDebugSystemObjects3::GetTotalNumberThreads, IDebugSystemObjects2::GetTotalNumberThreads, GetTotalNumberThreads method [Windows Debugging], IDebugSystemObjects4 interface, IDebugSystemObjects4 interface [Windows Debugging], GetTotalNumberThreads method, IDebugSystemObjects2, IDebugSystemObjects interface [Windows Debugging], GetTotalNumberThreads method, IDebugSystemObjects4::GetTotalNumberThreads, IDebugSystemObjects3::GetTotalNumberThreads
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
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
req.lib: dbgeng.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	dbgeng.h
apiname:
-	IDebugSystemObjects.GetTotalNumberThreads
-	IDebugSystemObjects2.GetTotalNumberThreads
-	IDebugSystemObjects3.GetTotalNumberThreads
-	IDebugSystemObjects4.GetTotalNumberThreads
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugSystemObjects2::GetTotalNumberThreads method


## -description


The <b>GetTotalNumberThreads</b> method returns the total number of <a href="https://msdn.microsoft.com/6182ca34-ee5e-47e9-82fe-29266397e3a8">threads</a> for all the <a href="https://msdn.microsoft.com/6182ca34-ee5e-47e9-82fe-29266397e3a8">processes</a> in the current target, in addition to the largest number of threads in any process for the current target.


## -syntax


````
HRESULT GetTotalNumberThreads(
  [out] PULONG Total,
  [out] PULONG LargestProcess
);
````


## -parameters




### -param Total [out]

Receives the total number of threads for all the processes in the current target.


### -param LargestProcess [out]

Receives the largest number of threads in any process for the current target.


## -returns



This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -remarks



For more information about threads, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558896">Threads and Processes</a>.



