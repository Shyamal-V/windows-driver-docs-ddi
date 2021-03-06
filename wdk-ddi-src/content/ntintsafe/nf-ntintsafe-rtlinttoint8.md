---
UID: NF:ntintsafe.RtlIntToInt8
title: RtlIntToInt8 function
author: windows-driver-content
description: Converts a value of type INT to a value of type INT8.
old-location: kernel\rtlinttoint8.htm
old-project: kernel
ms.assetid: ABE24C02-22C3-4F0A-B874-3079F70CA748
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: ntintsafe/RtlIntToInt8, RtlIntToInt8 function [Kernel-Mode Driver Architecture], kernel.rtlinttoint8, RtlIntToInt8
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntintsafe.h
req.include-header: 
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	Ntintsafe.h
apiname:
-	RtlIntToInt8
product: Windows
targetos: Windows
req.typenames: PUBLIC_OBJECT_TYPE_INFORMATION, *PPUBLIC_OBJECT_TYPE_INFORMATION
---

# RtlIntToInt8 function


## -description


Converts a value of type <b>INT</b> to a value of type <b>INT8</b>.


## -syntax


````
NTSTATUS RtlIntToInt8(
  _In_  INT  iOperand,
  _Out_ INT8 *pi8Result
);
````


## -parameters




### -param iOperand [in]

The value to be converted.


### -param pi8Result [out]

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

This function uses the following alternate name:

<ul>
<li>RtlInt32ToInt8
</li>
</ul>


