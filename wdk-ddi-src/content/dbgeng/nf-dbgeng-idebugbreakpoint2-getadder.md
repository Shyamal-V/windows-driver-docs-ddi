---
UID: NF:dbgeng.IDebugBreakpoint2.GetAdder
title: IDebugBreakpoint2::GetAdder method
author: windows-driver-content
description: The GetAdder method returns the client that owns the breakpoint.
old-location: debugger\getadder.htm
old-project: debugger
ms.assetid: f57abfc5-d6ae-474b-bea9-bfc53dff7f57
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugBreakpoint2::GetAdder, IDebugBreakpoint::GetAdder, IDebugBreakpoint interface [Windows Debugging], GetAdder method, GetAdder, debugger.getadder, dbgeng/IDebugBreakpoint2::GetAdder, ComOther_069dfd81-8ad8-4fe7-95c4-a3499c1b5512.xml, GetAdder method [Windows Debugging], IDebugBreakpoint, IDebugBreakpoint2, IDebugBreakpoint2 interface [Windows Debugging], GetAdder method, GetAdder method [Windows Debugging], IDebugBreakpoint interface, dbgeng/IDebugBreakpoint::GetAdder, GetAdder method [Windows Debugging], IDebugBreakpoint2 interface
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
-	IDebugBreakpoint.GetAdder
-	IDebugBreakpoint2.GetAdder
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugBreakpoint2::GetAdder method


## -description


The <b>GetAdder</b> method returns the client that owns the breakpoint.


## -syntax


````
HRESULT GetAdder(
  [out] PDEBUG_CLIENT *Adder
);
````


## -parameters




### -param Adder [out]

An <a href="..\dbgeng\nn-dbgeng-idebugclient.md">IDebugClient</a> interface pointer to the client object that added the breakpoint.


## -returns



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
 

This method can also return error values.  For more information, see <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a>.




## -remarks



The client that owns the breakpoint is the client that created the breakpoint by using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537856">AddBreakpoint</a> method.  A breakpoint might not have an owner. If a breakpoint does not have an owner, <i>Adder</i> is set to <b>NULL</b>.

For more information about how to use breakpoints, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560075">Using Breakpoints</a>.



