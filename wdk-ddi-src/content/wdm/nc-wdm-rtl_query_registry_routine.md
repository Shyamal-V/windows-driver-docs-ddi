---
UID: NC:wdm.RTL_QUERY_REGISTRY_ROUTINE
title: RTL_QUERY_REGISTRY_ROUTINE
author: windows-driver-content
description: The QueryRoutine routine provides information about a registry value that was requested in a preceding call to the RtlQueryRegistryValues routine.
old-location: kernel\queryroutine.htm
old-project: kernel
ms.assetid: 28f9cfcd-ed2e-4760-9016-3542c27cb347
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: kernel.queryroutine, QueryRoutine routine [Kernel-Mode Driver Architecture], QueryRoutine, RTL_QUERY_REGISTRY_ROUTINE, RTL_QUERY_REGISTRY_ROUTINE, wdm/QueryRoutine, DrvrRtns_a5cd47f1-6d3c-495e-a83d-ccbd276c1728.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Desktop
req.target-min-winverclnt: Supported starting with Windows 2000.
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
req.irql: Called at PASSIVE_LEVEL.
topictype:
-	APIRef
-	kbSyntax
apitype:
-	UserDefined
apilocation:
-	Wdm.h
apiname:
-	QueryRoutine
product: Windows
targetos: Windows
req.typenames: "*PWDI_TYPE_PMK_NAME, WDI_TYPE_PMK_NAME"
req.product: Windows 10 or later.
---

# RTL_QUERY_REGISTRY_ROUTINE callback


## -description


The <i>QueryRoutine</i> routine provides information about a registry value that was requested in a preceding call to the <a href="..\wdm\nf-wdm-rtlqueryregistryvalues.md">RtlQueryRegistryValues</a> routine.


## -prototype


````
RTL_QUERY_REGISTRY_ROUTINE QueryRoutine;

NTSTATUS QueryRoutine(
  _In_     PWSTR ValueName,
  _In_     ULONG ValueType,
  _In_     PVOID ValueData,
  _In_     ULONG ValueLength,
  _In_opt_ PVOID Context,
  _In_opt_ PVOID EntryContext
)
{ ... }
````


## -parameters




### -param ValueName [in]

Specifies the registry key that is associated with the requested registry value. This parameter is a pointer to a null-terminated, Unicode string that contains the key.


### -param ValueType [in]

Specifies the type of registry value that is stored with the specified registry key. For more information registry value types, see the definition of the <i>Type</i> parameter in <a href="..\wdm\ns-wdm-_key_value_basic_information.md">KEY_VALUE_BASIC_INFORMATION</a>.


### -param ValueData [in]

A pointer to the data value that is associated with the specified registry key. The driver must treat this value as read-only. For more information about the type of value data that <i>ValueData</i> points to, see the definition of the <i>Type</i> parameter in <a href="..\wdm\ns-wdm-_key_value_basic_information.md">KEY_VALUE_BASIC_INFORMATION</a>.


### -param ValueLength [in]

Specifies the length, in bytes, of the value that <i>ValueData</i> points to.


### -param Context [in, optional]

Specifies the <i>Context</i> parameter value that the driver specified in the preceding call to <b>RtlQueryRegistryValues</b>.


### -param EntryContext [in, optional]

Specifies an <b>EntryContext</b> value in a <i>QueryTable</i> array element that the driver specified in the preceding call to <b>RtlQueryRegistryValues</b>.


## -returns



<i>QueryRoutine</i> returns STATUS_SUCCESS if the call is successful. Otherwise, it returns an appropriate error status code. Use only status codes that are defined in the Ntstatus.h header file.




## -remarks



A kernel-mode driver implements a <i>QueryRoutine</i> routine. This routine is called by the <a href="..\wdm\nf-wdm-rtlqueryregistryvalues.md">RtlQueryRegistryValues</a> routine.

To obtain information about one or more registry values, the driver calls <b>RtlQueryRegistryValues</b> and passes a pointer, as an input parameter, to an array of <b>RTL_QUERY_REGISTRY_TABLE</b> structures. Each structure in this array contains a pointer to a driver-implemented <i>QueryRoutine</i> routine and a request for information about a particular registry value. For each structure in the array, <b>RtlQueryRegistryValues</b> calls the specified <i>QueryRoutine</i> routine and passes to this routine a set of parameters that contain the requested information about the specified registry value.

For more information about the <b>RTL_QUERY_REGISTRY_TABLE</b> structure, see <a href="..\wdm\nf-wdm-rtlqueryregistryvalues.md">RtlQueryRegistryValues</a>.


#### Examples

To define a <i>QueryRoutine</i> callback routine, you must first provide a function declaration that identifies the type of callback routine you're defining. Windows provides a set of callback function types for drivers. Declaring a function using the callback function types helps <a href="https://msdn.microsoft.com/2F3549EF-B50F-455A-BDC7-1F67782B8DCA">Code Analysis for Drivers</a>, <a href="https://msdn.microsoft.com/74feeb16-387c-4796-987a-aff3fb79b556">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it's a requirement for writing drivers for the Windows operating system.

For example, to define a <i>QueryRoutine</i> callback routine that is named <code>MyQueryRoutine</code>, use the RTL_QUERY_REGISTRY_ROUTINE type as shown in this code example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>RTL_QUERY_REGISTRY_ROUTINE MyQueryRoutine;</pre>
</td>
</tr>
</table></span></div>
Then, implement your callback routine as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>_Use_decl_annotations_
NTSTATUS
  MyQueryRoutine(
    PWSTR ValueName,
    ULONG ValueType,
    PVOID ValueData,
    ULONG ValueLength,
    PVOID Context,
    PVOID EntryContext
    )
  {
      // Function body
  }</pre>
</td>
</tr>
</table></span></div>
The RTL_QUERY_REGISTRY_ROUTINE function type is defined in the Wdm.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition. The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the RTL_QUERY_REGISTRY_ROUTINE function type in the header file are used. For more information about the requirements for function declarations, see <a href="https://msdn.microsoft.com/3260b53e-82be-4dbc-8ac5-d0e52de77f9d">Declaring Functions by Using Function Role Types for WDM Drivers</a>. For information about _Use_decl_annotations_, see <a href="http://go.microsoft.com/fwlink/p/?linkid=286697">Annotating Function Behavior</a>.

<div class="code"></div>



## -see-also

<a href="..\wdm\nf-wdm-rtlqueryregistryvalues.md">RtlQueryRegistryValues</a>



<a href="..\wdm\ns-wdm-_key_value_basic_information.md">KEY_VALUE_BASIC_INFORMATION</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20QueryRoutine routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

