---
UID: NF:wdm.READ_REGISTER_ULONG
title: READ_REGISTER_ULONG function
author: windows-driver-content
description: The READ_REGISTER_ULONG routine reads a ULONG value from the specified register address.
old-location: kernel\read_register_ulong.htm
old-project: kernel
ms.assetid: a462734c-cac6-4de0-95c1-810766ef1644
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: kernel.read_register_ulong, k103_c2da9866-18ac-438b-aa32-991d1bda139f.xml, wdm/READ_REGISTER_ULONG, READ_REGISTER_ULONG, READ_REGISTER_ULONG routine [Kernel-Mode Driver Architecture]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: Any level (see Remarks section)
topictype:
-	APIRef
-	kbSyntax
apitype:
-	DllExport
apilocation:
-	NtosKrnl.exe
apiname:
-	READ_REGISTER_ULONG
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# READ_REGISTER_ULONG function


## -description


The <b>READ_REGISTER_ULONG</b> routine reads a ULONG value from the specified register address.


## -syntax


````
ULONG READ_REGISTER_ULONG(
  _In_ PULONG Register
);
````


## -parameters




### -param Register [in]

Pointer to the register address, which must be a mapped range in memory space. 


## -returns



<b>READ_REGISTER_ULONG</b> returns the ULONG value read from the specified register address.




## -remarks



Callers of <b>READ_REGISTER_ULONG</b> can be running at any IRQL, assuming the <i>Register</i> is resident, mapped device memory.



