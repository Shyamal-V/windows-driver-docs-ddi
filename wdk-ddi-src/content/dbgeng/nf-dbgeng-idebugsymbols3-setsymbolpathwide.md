---
UID: NF:dbgeng.IDebugSymbols3.SetSymbolPathWide
title: IDebugSymbols3::SetSymbolPathWide method
author: windows-driver-content
description: The SetSymbolPathWide method sets the symbol path.
old-location: debugger\setsymbolpathwide.htm
old-project: debugger
ms.assetid: 44ee3342-3677-4eee-8ddf-d0a01e9bb309
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: SetSymbolPathWide, debugger.setsymbolpathwide, SetSymbolPathWide method [Windows Debugging], IDebugSymbols3, dbgeng/IDebugSymbols3::SetSymbolPathWide, IDebugSymbols3::SetSymbolPathWide, SetSymbolPathWide method [Windows Debugging], IDebugSymbols3 interface, IDebugSymbols3 interface [Windows Debugging], SetSymbolPathWide method
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
-	IDebugSymbols3.SetSymbolPathWide
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugSymbols3::SetSymbolPathWide method


## -description


The <b>SetSymbolPathWide</b>  method sets the symbol path.


## -syntax


````
HRESULT SetSymbolPathWide(
  [in] PCWSTR Path
);
````


## -parameters




### -param Path [in]

Specifies the new symbol path.  This is a string that contains symbol path elements separated by semicolons (;).  Each symbol path element can specify either a directory or a symbol server.


## -returns



This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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



For more information about manipulating the symbol path, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560150">Using Symbols</a>.  For an overview of the symbol path and its syntax, see <a href="https://msdn.microsoft.com/705df98f-717f-40ad-a424-101826970691">Symbol Path</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff549155">GetSymbolPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538110">AppendSymbolPath</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols3::SetSymbolPathWide method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

