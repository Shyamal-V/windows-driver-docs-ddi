---
UID: NF:ntifs.SecMakeSPNEx
title: SecMakeSPNEx function
author: windows-driver-content
description: SecMakeSPNEx creates a service provider name string that can be used when communicating with specific security service providers.
old-location: ifsk\secmakespnex.htm
old-project: ifsk
ms.assetid: 5000be89-144c-405c-93ea-3e9372e0a677
ms.author: windowsdriverdev
ms.date: 2/7/2018
ms.keywords: ntifs/SecMakeSPNEx, ifsk.secmakespnex, SecMakeSPNEx function [Installable File System Drivers], SecMakeSPNEx, ksecddref_3c4441b9-ed78-473f-ac3c-35a644018499.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h, FltKernel.h
req.target-type: Universal
req.target-min-winverclnt: This function is only available on Microsoft Windows XP and later.
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
req.lib: Ksecdd.lib
req.dll: 
req.irql: "<= APC_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	LibDef
apilocation:
-	Ksecdd.lib
-	Ksecdd.dll
apiname:
-	SecMakeSPNEx
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# SecMakeSPNEx function


## -description


<b>SecMakeSPNEx</b> creates a service provider name string that can be used when communicating with specific security service providers. 


## -syntax


````
NTSTATUS SecMakeSPNEx(
  _In_    PUNICODE_STRING ServiceClass,
  _In_    PUNICODE_STRING ServiceName,
  _In_    PUNICODE_STRING InstanceName,
  _In_    USHORT          InstancePort,
  _In_    PUNICODE_STRING Referrer,
  _In_    PUNICODE_STRING TargetInfo,
  _Inout_ PUNICODE_STRING Spn,
  _Out_   PULONG          Length,
  _In_    BOOLEAN         Allocate
);
````


## -parameters




### -param ServiceClass [in]

A pointer to a Unicode string specifying the service class for the security service provider. 


### -param ServiceName [in]

A pointer to a Unicode string specifying the service name for the security service provider. 


### -param OPTIONAL

TBD


### -param Spn [in, out]

A pointer to a Unicode string for storing the security service provider name string created by this function.


### -param Allocate [in]

A Boolean variable indicating if the memory for storing the <i>Spn</i> Unicode string should be allocated by this function. If this parameter is true, memory for <i>Spn</i> will be allocated from paged pool.


#### - InstanceName [in]

A pointer to an optional Unicode string specifying the instance name for connecting with the security service provider. 


#### - InstancePort [in]

An optional variable specifying the instance port for connecting with the security service provider. 


#### - Length [out]

A pointer to an optional variable for storing the length of the security service provider name string created by this function.


#### - Referrer [in]

A pointer to an optional Unicode string specifying the referrer name for connecting with the security service provider. 


#### - TargetInfo [in]

A pointer to an optional Unicode string specifying target information for connecting with the security service provider. 


## -returns



<b>SecMakeSPNEx</b> returns STATUS_SUCCESS on success or one of the following error codes on failure: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The <i>Allocate</i> parameter was set to false and one of the following conditions occurred:

The <i>Spn </i>parameter was a null pointer.

The maximum length for the <i>Spn</i> Unicode string parameter was too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A total length of the <i>Spn</i> parameter exceeds 65535 bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The <i>Allocate</i> parameter was set to true, but the memory allocation request failed.

</td>
</tr>
</table>
 




## -remarks



<b>SecMakeSPNEx</b> is an enhanced version of <b>SecMakeSPN</b>. 




## -see-also

<a href="..\ntifs\nf-ntifs-secmakespnex2.md">SecMakeSPNEx2</a>



<a href="..\ntifs\nf-ntifs-secmakespn.md">SecMakeSPN</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20SecMakeSPNEx function%20 RELEASE:%20(2/7/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

