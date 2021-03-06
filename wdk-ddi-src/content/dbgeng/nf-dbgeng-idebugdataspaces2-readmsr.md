---
UID: NF:dbgeng.IDebugDataSpaces2.ReadMsr
title: IDebugDataSpaces2::ReadMsr method
author: windows-driver-content
description: The ReadMsr method reads a specified Model-Specific Register (MSR).
old-location: debugger\readmsr2.htm
old-project: debugger
ms.assetid: 3ffe53d9-ea57-4561-a889-e6369ef0d5d3
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugDataSpaces4 interface [Windows Debugging], ReadMsr method, dbgeng/IDebugDataSpaces2::ReadMsr, ReadMsr method [Windows Debugging], IDebugDataSpaces4 interface, IDebugDataSpaces3::ReadMsr, IDebugDataSpaces2 interface [Windows Debugging], ReadMsr method, IDebugDataSpaces2::ReadMsr, IDebugDataSpaces3 interface [Windows Debugging], ReadMsr method, ReadMsr method [Windows Debugging], IDebugDataSpaces2 interface, ReadMsr, IDebugDataSpaces2, ReadMsr method [Windows Debugging], IDebugDataSpaces3 interface, dbgeng/IDebugDataSpaces3::ReadMsr, IDebugDataSpaces4::ReadMsr, IDebugDataSpaces interface [Windows Debugging], ReadMsr method, ReadMsr method [Windows Debugging], IDebugDataSpaces::ReadMsr, dbgeng/IDebugDataSpaces::ReadMsr, ReadMsr method [Windows Debugging], IDebugDataSpaces interface, IDebugDataSpaces, debugger.readmsr2, IDebugDataSpaces_ad5999a9-949f-4771-b0b9-16fa1b79ac10.xml, dbgeng/IDebugDataSpaces4::ReadMsr
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
-	IDebugDataSpaces.ReadMsr
-	IDebugDataSpaces2.ReadMsr
-	IDebugDataSpaces3.ReadMsr
-	IDebugDataSpaces4.ReadMsr
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugDataSpaces2::ReadMsr method


## -description


The <b>ReadMsr</b> method reads a specified Model-Specific Register (MSR).


## -syntax


````
HRESULT ReadMsr(
  [in]  ULONG    Msr,
  [out] PULONG64 Value
);
````


## -parameters




### -param Msr [in]

Specifies the MSR address.


### -param Value [out]

Receives the value of the MSR.


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
 

This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.




## -remarks



This method is only available in kernel-mode debugging.

For details on the addresses and values of MSRs, see the processor documentation.



