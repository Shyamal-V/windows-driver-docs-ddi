---
UID: NE:wdftypes._WDF_TRI_STATE
title: "_WDF_TRI_STATE"
author: windows-driver-content
description: The WDF_TRI_STATE enumeration type defines three values that the framework uses for some structure members and function parameters.
old-location: wdf\wdf_tri_state.htm
old-project: wdf
ms.assetid: 8ea6e373-225d-4fcd-abcf-c19b07f9f5d8
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: WDF_TRI_STATE, wdftypes/PWDF_TRI_STATE, *PWDF_TRI_STATE, PWDF_TRI_STATE, wudfddi_types/WDF_TRI_STATE, wdftypes/WdfUseDefault, wdftypes/WDF_TRI_STATE, WdfTrue, wudfddi_types/WdfTrue, wudfddi_types/WdfUseDefault, _WDF_TRI_STATE, wdftypes/WdfTrue, WDF_TRI_STATE enumeration, wdftypes/WdfFalse, wudfddi_types/PWDF_TRI_STATE, WdfFalse, PWDF_TRI_STATE enumeration pointer, wdf.wdf_tri_state, wudfddi_types/WdfFalse, kmdf.wdf_tri_state, WdfUseDefault, DFGenObjectRef_83855649-9d84-4f8c-9685-5e5321209b4d.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdftypes.h
req.include-header: Wdf.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: Any level
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	wdftypes.h
-	wudfddi_types.h
apiname:
-	WDF_TRI_STATE
product: Windows
targetos: Windows
req.typenames: WDF_TRI_STATE, *PWDF_TRI_STATE
req.product: Windows 10 or later.
---

# _WDF_TRI_STATE enumeration


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The WDF_TRI_STATE enumeration type defines three values that the framework uses for some structure members and function parameters.


## -syntax


````
typedef enum _WDF_TRI_STATE { 
  WdfFalse       = FALSE,
  WdfTrue        = TRUE,
  WdfUseDefault  = 2
} WDF_TRI_STATE, *PWDF_TRI_STATE;
````


## -enum-fields




### -field WdfFalse

The meaning of this enumerator is specific to its use as a structure member or function parameter.


### -field WdfTrue

The meaning of this enumerator is specific to its use as a structure member or function parameter.


### -field WdfUseDefault

The meaning of this enumerator is specific to its use as a structure member or function parameter.


## -remarks



The WDF_TRI_STATE enumeration type is available in version 1.0 and later versions of KMDF.



