---
UID: NF:dbgeng.IDebugSystemObjects2.GetNumberThreads
title: IDebugSystemObjects2::GetNumberThreads method
author: windows-driver-content
description: The GetNumberThreads method returns the number of threads in the current process.
old-location: debugger\getnumberthreads.htm
old-project: debugger
ms.assetid: f56da2d0-4c4c-4302-a87b-c672dec25d9f
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugSystemObjects4::GetNumberThreads, GetNumberThreads method [Windows Debugging], IDebugSystemObjects3 interface, GetNumberThreads, IDebugSystemObjects interface [Windows Debugging], GetNumberThreads method, GetNumberThreads method [Windows Debugging], IDebugSystemObjects interface, GetNumberThreads method [Windows Debugging], IDebugSystemObjects4 interface, dbgeng/IDebugSystemObjects2::GetNumberThreads, GetNumberThreads method [Windows Debugging], IDebugSystemObjects2 interface, dbgeng/IDebugSystemObjects4::GetNumberThreads, debugger.getnumberthreads, dbgeng/IDebugSystemObjects3::GetNumberThreads, IDebugSystemObjects4 interface [Windows Debugging], GetNumberThreads method, IDebugSystemObjects, GetNumberThreads method [Windows Debugging], IDebugSystemObjects_47d86764-4881-4178-97fa-d6c8732dbb1a.xml, IDebugSystemObjects::GetNumberThreads, IDebugSystemObjects3::GetNumberThreads, IDebugSystemObjects2 interface [Windows Debugging], GetNumberThreads method, IDebugSystemObjects3 interface [Windows Debugging], GetNumberThreads method, IDebugSystemObjects2::GetNumberThreads, dbgeng/IDebugSystemObjects::GetNumberThreads, IDebugSystemObjects2
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
-	IDebugSystemObjects.GetNumberThreads
-	IDebugSystemObjects2.GetNumberThreads
-	IDebugSystemObjects3.GetNumberThreads
-	IDebugSystemObjects4.GetNumberThreads
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugSystemObjects2::GetNumberThreads method


## -description


The <b>GetNumberThreads</b> method returns the number of <a href="https://msdn.microsoft.com/6182ca34-ee5e-47e9-82fe-29266397e3a8">threads</a> in the current process.


## -syntax


````
HRESULT GetNumberThreads(
  [out] PULONG Number
);
````


## -parameters




### -param Number [out]

Receives the number of threads in the current process.


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



In kernel-mode debugging, there is a virtual thread representing each processor.

In user-mode debugging, the number of threads changes with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550713">IDebugEventCallbacks::CreateThread</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff550730">IDebugEventCallbacks::ExitThread</a> events.

For more information about threads, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558896">Threads and Processes</a>.



