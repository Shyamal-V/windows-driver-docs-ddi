---
UID: NS:dbgeng._DEBUG_GET_TEXT_COMPLETIONS_OUT
title: "_DEBUG_GET_TEXT_COMPLETIONS_OUT"
author: windows-driver-content
description: Defines information about text completions to get.
old-location: debugger\debug_get_text_completions_out.htm
old-project: debugger
ms.assetid: 09F3A720-C039-4C8D-84A4-8AF071E1FFB0
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: PDEBUG_GET_TEXT_COMPLETIONS_OUT structure pointer [Windows Debugging], _DEBUG_GET_TEXT_COMPLETIONS_OUT, DEBUG_GET_TEXT_COMPLETIONS_IS_DOT_COMMAND, DEBUG_GET_TEXT_COMPLETIONS_OUT, debugger.debug_get_text_completions_out, PDEBUG_GET_TEXT_COMPLETIONS_OUT, DEBUG_GET_TEXT_COMPLETIONS_IS_SYMBOL, *PDEBUG_GET_TEXT_COMPLETIONS_OUT, dbgeng/PDEBUG_GET_TEXT_COMPLETIONS_OUT, DEBUG_GET_TEXT_COMPLETIONS_OUT structure [Windows Debugging], DEBUG_GET_TEXT_COMPLETIONS_IS_EXTENSION_COMMAND, dbgeng/DEBUG_GET_TEXT_COMPLETIONS_OUT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dbgeng.h
req.include-header: DbgEng.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	DbgEng.h
apiname:
-	DEBUG_GET_TEXT_COMPLETIONS_OUT
product: Windows
targetos: Windows
req.typenames: "*PDEBUG_GET_TEXT_COMPLETIONS_OUT, DEBUG_GET_TEXT_COMPLETIONS_OUT"
---

# _DEBUG_GET_TEXT_COMPLETIONS_OUT structure


## -description


Defines information about text completions to get. 


## -syntax


````
typedef struct _DEBUG_GET_TEXT_COMPLETIONS_OUT {
  ULONG   Flags;
  ULONG   ReplaceIndex;
  ULONG   MatchCount;
  ULONG   Reserved1;
  ULONG64 Reserved2[2];
} DEBUG_GET_TEXT_COMPLETIONS_OUT, *PDEBUG_GET_TEXT_COMPLETIONS_OUT;
````


## -struct-fields




### -field Flags

Flags. Valid flag values include the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEBUG_GET_TEXT_COMPLETIONS_IS_DOT_COMMAND"></a><a id="debug_get_text_completions_is_dot_command"></a><dl>
<dt><b>DEBUG_GET_TEXT_COMPLETIONS_IS_DOT_COMMAND</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Is dot command. Dot commands begin with a period (.).

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_GET_TEXT_COMPLETIONS_IS_EXTENSION_COMMAND"></a><a id="debug_get_text_completions_is_extension_command"></a><dl>
<dt><b>DEBUG_GET_TEXT_COMPLETIONS_IS_EXTENSION_COMMAND</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Is extension command.

</td>
</tr>
<tr>
<td width="40%"><a id="DEBUG_GET_TEXT_COMPLETIONS_IS_SYMBOL"></a><a id="debug_get_text_completions_is_symbol"></a><dl>
<dt><b>DEBUG_GET_TEXT_COMPLETIONS_IS_SYMBOL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Is symbol.

</td>
</tr>
</table>
 


### -field ReplaceIndex

The index of the replace location.


### -field MatchCount

Count value of matches.


### -field Reserved1

Reserved.


### -field Reserved2

Reserved.

