---
UID: NF:ntintsafe.RtlULongLongToUInt
title: RtlULongLongToUInt function
author: windows-driver-content
description: Converts a value of type ULONGLONG to a value of type UINT.
old-location: kernel\rtlulonglongtouint.htm
old-project: kernel
ms.assetid: CC69FD37-27DE-47AD-B509-DB659B906248
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: RtlULongLongToUInt, RtlULongLongToUInt function [Kernel-Mode Driver Architecture], ntintsafe/RtlULongLongToUInt, kernel.rtlulonglongtouint
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
-	RtlULongLongToUInt
product: Windows
targetos: Windows
req.typenames: PUBLIC_OBJECT_TYPE_INFORMATION, *PPUBLIC_OBJECT_TYPE_INFORMATION
---

# RtlULongLongToUInt function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>UINT</b>.


## -syntax


````
NTSTATUS RtlULongLongToUInt(
  _In_  ULONGLONG ullOperand,
  _Out_ UINT      *puResult
);
````


## -parameters




### -param ullOperand [in]

The value to be converted.


### -param puResult [out]

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



