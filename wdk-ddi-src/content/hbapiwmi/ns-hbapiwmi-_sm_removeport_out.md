---
UID: NS:hbapiwmi._SM_RemovePort_OUT
title: "_SM_RemovePort_OUT"
author: windows-driver-content
description: The SM_RemovePort_OUT structure is used to receive output parameters from the SM_RemovePort WMI method.
old-location: storage\sm_removeport_out.htm
old-project: storage
ms.assetid: 7ca1bd9f-8fd4-4d9d-8571-4d6e4b721f3b
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: hbapiwmi/SM_RemovePort_OUT, SM_RemovePort_OUT structure [Storage Devices], SM_RemovePort_OUT, *PSM_RemovePort_OUT, PSM_RemovePort_OUT structure pointer [Storage Devices], storage.sm_removeport_out, _SM_RemovePort_OUT, PSM_RemovePort_OUT, hbapiwmi/PSM_RemovePort_OUT, structs-Fibre_00eb7ab2-9a70-4e22-8b57-1468f52bfe02.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hbapiwmi.h
req.include-header: Hbapiwmi.h
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
-	hbapiwmi.h
apiname:
-	SM_RemovePort_OUT
product: Windows
targetos: Windows
req.typenames: SM_RemovePort_OUT, *PSM_RemovePort_OUT
---

# _SM_RemovePort_OUT structure


## -description


The SM_RemovePort_OUT structure is used to receive output parameters from the SM_RemovePort WMI method.


## -syntax


````
typedef struct _SM_RemovePort_OUT {
  ULONG HBAStatus;
} SM_RemovePort_OUT, *PSM_RemovePort_OUT;
````


## -struct-fields




### -field HBAStatus

The status of the operation. For a list of allowed values and their descriptions, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a>.


## -remarks



The WMI tool suite generates a declaration of the SM_RemovePort_OUT structure in <i>Hbapiwmi.h</i> when it compiles the MS_SM_EventControl WMI class.



