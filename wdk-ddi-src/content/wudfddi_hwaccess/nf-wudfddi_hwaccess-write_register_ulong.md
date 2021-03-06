---
UID: NF:wudfddi_hwaccess.WRITE_REGISTER_ULONG
title: WRITE_REGISTER_ULONG function
author: windows-driver-content
description: The WRITE_REGISTER_ULONG routine writes a ULONG value to the specified address.
old-location: wdf\write_register_ulong.htm
old-project: wdf
ms.assetid: E5C5DAEA-9F4E-4202-90BE-A8D41EE03BDA
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: umdf.write_register_ulong, WRITE_REGISTER_ULONG function, wudfddi_hwaccess/WRITE_REGISTER_ULONG, WRITE_REGISTER_ULONG, wdf.write_register_ulong
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wudfddi_hwaccess.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
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
-	Wudfddi_hwaccess.h
apiname:
-	WRITE_REGISTER_ULONG
product: Windows
targetos: Windows
req.typenames: "*PUMDF_IO_TARGET_OPEN_PARAMS, UMDF_IO_TARGET_OPEN_PARAMS"
req.product: Windows 10 or later.
---

# WRITE_REGISTER_ULONG function


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>WRITE_REGISTER_ULONG</b> routine writes a ULONG value to the specified address.


## -syntax


````
void WRITE_REGISTER_ULONG(
  _In_ IWDFDevice3 *pDevice,
  _In_ PULONG      Register,
  _In_ ULONG       Value
);
````


## -parameters




### -param pDevice [in]

Specifies a pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfdevice3.md">IWDFDevice3</a> interface for the device object of the device to access.


### -param Register [in]

A pointer to the register, which must be a mapped range in memory space.


### -param Value [in]

Specifies a ULONG value to write to the register.


## -returns



This function does not return a value.




## -remarks



For more information, see <a href="https://msdn.microsoft.com/A0640E60-B0DF-4CAD-B292-CC1875EF7F7D">Reading and Writing to Device Registers in UMDF 1.x Drivers</a>.



