---
UID: NF:dbgeng.IDebugSymbols2.GetTypeOptions
title: IDebugSymbols2::GetTypeOptions method
author: windows-driver-content
description: The GetTypeOptions method returns the type formatting options for output generated by the engine.
old-location: debugger\gettypeoptions.htm
old-project: debugger
ms.assetid: a21442e5-8237-4d00-8d8a-6fabd6cc0db2
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: dbgeng/IDebugSymbols2::GetTypeOptions, IDebugSymbols2::GetTypeOptions, IDebugSymbols3::GetTypeOptions, dbgeng/IDebugSymbols3::GetTypeOptions, GetTypeOptions method [Windows Debugging], IDebugSymbols3 interface, IDebugSymbols3 interface [Windows Debugging], GetTypeOptions method, IDebugSymbols2, IDebugSymbols_ea8a630e-a7a9-40eb-9127-76fd876bf253.xml, GetTypeOptions method [Windows Debugging], IDebugSymbols2 interface, debugger.gettypeoptions, GetTypeOptions method [Windows Debugging], GetTypeOptions, IDebugSymbols2 interface [Windows Debugging], GetTypeOptions method
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
-	IDebugSymbols2.GetTypeOptions
-	IDebugSymbols3.GetTypeOptions
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugSymbols2::GetTypeOptions method


## -description


The <b>GetTypeOptions</b> method returns the type formatting options for output generated by the engine.


## -syntax


````
HRESULT GetTypeOptions(
  [out] PULONG Options
);
````


## -parameters




### -param Options [out]

Receives the type formatting options.  <i>Options</i> is a bit-set; for a description of the bit flags, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff541712">DEBUG_TYPEOPTS_XXX</a>.


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



After the type options have been changed, for each client the engine sends out notification to that client's <a href="..\dbgeng\nn-dbgeng-idebugeventcallbacks.md">IDebugEventCallbacks</a> by passing the DEBUG_CES_TYPE_OPTIONS flag to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550692">IDebugEventCallbacks::ChangeSymbolState</a> method.

For more information about types, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558931">Types</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537949">AddTypeOptions</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554551">RemoveTypeOptions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556874">SetTypeOptions</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols2::GetTypeOptions method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
