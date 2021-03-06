---
UID: NF:dbgeng.IDebugRegisters.OutputRegisters
title: IDebugRegisters::OutputRegisters method
author: windows-driver-content
description: The OutputRegisters method formats and sends the target's registers to the clients as output.
old-location: debugger\outputregisters.htm
old-project: debugger
ms.assetid: d1354ab7-4d7d-4cc2-8e30-763d8b881a11
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugRegisters::OutputRegisters, OutputRegisters method [Windows Debugging], IDebugRegisters2 interface, IDebugRegisters2::OutputRegisters, OutputRegisters method [Windows Debugging], debugger.outputregisters, IDebugRegisters interface [Windows Debugging], OutputRegisters method, IDebugRegisters_65d62961-afc5-4609-86d2-c55757fe6ce1.xml, IDebugRegisters, OutputRegisters, dbgeng/IDebugRegisters::OutputRegisters, OutputRegisters method [Windows Debugging], IDebugRegisters interface, IDebugRegisters2 interface [Windows Debugging], OutputRegisters method, dbgeng/IDebugRegisters2::OutputRegisters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: DbgEng.h
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
-	IDebugRegisters.OutputRegisters
-	IDebugRegisters2.OutputRegisters
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugRegisters::OutputRegisters method


## -description


The <b>OutputRegisters</b> method formats and sends the target's <a href="https://msdn.microsoft.com/library/windows/hardware/ff554369">registers</a> to the clients as output.


## -syntax


````
HRESULT OutputRegisters(
  [in] ULONG OutputControl,
  [in] ULONG Flags
);
````


## -parameters




### -param OutputControl [in]

Specifies which clients should be sent the output of the formatted registers.  See <a href="https://msdn.microsoft.com/library/windows/hardware/ff541517">DEBUG_OUTCTL_XXX</a> for possible values.


### -param Flags [in]

Specifies which set of registers to print.  This can either be DEBUG_REGISTERS_DEFAULT to print commonly used registers, DEBUG_REGISTERS_ALL to print all the sets of registers, or a combination of the values listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
DEBUG_REGISTERS_INT32

</td>
<td>
Print the 32-bit register set.

</td>
</tr>
<tr>
<td>
DEBUG_REGISTERS_INT64

</td>
<td>
Print the 64-bit register set.

</td>
</tr>
<tr>
<td>
DEBUG_REGISTERS_FLOAT

</td>
<td>
Print the floating-point register set.

</td>
</tr>
</table>
 


## -returns



This list does not contain all the errors that might occur.  For a list of possible errors, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff549771">HRESULT Values</a>.

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



The registers are formatted in a way that is specific to the target architecture's register set.

The method <a href="https://msdn.microsoft.com/library/windows/hardware/ff553245">OutputRegisters2</a> performs the same task as this method but also allows the register source to be specified.

For an overview of the <a href="..\dbgeng\nn-dbgeng-idebugregisters.md">IDebugRegisters</a> interface and other register-related methods, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff554369">Registers</a>.  For details on sending output to the clients, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff550971">Input and Output</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff553245">OutputRegisters2</a>



<a href="..\dbgeng\nn-dbgeng-idebugregisters.md">IDebugRegisters</a>



<a href="..\dbgeng\nn-dbgeng-idebugregisters2.md">IDebugRegisters2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugRegisters::OutputRegisters method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

