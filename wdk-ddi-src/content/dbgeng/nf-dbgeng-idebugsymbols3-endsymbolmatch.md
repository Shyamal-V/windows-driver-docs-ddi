---
UID: NF:dbgeng.IDebugSymbols3.EndSymbolMatch
title: IDebugSymbols3::EndSymbolMatch method
author: windows-driver-content
description: The EndSymbolMatch method releases the resources used by a symbol search.
old-location: debugger\endsymbolmatch.htm
old-project: debugger
ms.assetid: 02cc9db2-173a-4d5d-a465-098391336100
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugSymbols2 interface [Windows Debugging], EndSymbolMatch method, EndSymbolMatch method [Windows Debugging], IDebugSymbols2 interface, EndSymbolMatch method [Windows Debugging], IDebugSymbols3 interface, IDebugSymbols3::EndSymbolMatch, debugger.endsymbolmatch, dbgeng/IDebugSymbols2::EndSymbolMatch, EndSymbolMatch, EndSymbolMatch method [Windows Debugging], IDebugSymbols interface, IDebugSymbols2::EndSymbolMatch, IDebugSymbols_1661cc8a-ad5c-4cd3-83fe-f829bd07e453.xml, IDebugSymbols2, IDebugSymbols3, dbgeng/IDebugSymbols::EndSymbolMatch, IDebugSymbols interface [Windows Debugging], EndSymbolMatch method, IDebugSymbols::EndSymbolMatch, dbgeng/IDebugSymbols3::EndSymbolMatch, IDebugSymbols, EndSymbolMatch method [Windows Debugging], IDebugSymbols3 interface [Windows Debugging], EndSymbolMatch method
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
-	IDebugSymbols.EndSymbolMatch
-	IDebugSymbols2.EndSymbolMatch
-	IDebugSymbols3.EndSymbolMatch
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugSymbols3::EndSymbolMatch method


## -description


The <b>EndSymbolMatch</b> method releases the resources used by a symbol search.


## -syntax


````
HRESULT EndSymbolMatch(
  [in] ULONG64 Handle
);
````


## -parameters




### -param Handle [in]

Specifies the handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff558815">StartSymbolMatch</a> when the search was initialized.


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



This method releases the resources held by the engine during a symbol search.  After these resources are released, the handle becomes invalid, so it must not be passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff547856">GetNextSymbolMatch</a> after it has been passed to this method.

For more information about symbols, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558824">Symbols</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff547856">GetNextSymbolMatch</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols.md">IDebugSymbols</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff558815">StartSymbolMatch</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols::EndSymbolMatch method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

