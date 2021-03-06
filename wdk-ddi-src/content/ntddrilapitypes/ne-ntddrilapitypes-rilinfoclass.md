---
UID: NE:ntddrilapitypes.RILINFOCLASS
title: RILINFOCLASS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilinfoclass.htm
old-project: netvista
ms.assetid: 2e4bd8bd-ce7e-4eb4-ac0d-68fb8890eb26
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: RILINFOCLASS, RILINFOCLASS enumeration [Network Drivers Starting with Windows Vista], RIL_INFOCLASS_PACKETACCESS, RIL_INFOCLASS_DATACIRCUITSYNC, RIL_INFOCLASS_DATA, ntddrilapitypes/RILINFOCLASS, ntddrilapitypes/RIL_INFOCLASS_PADACCESS, RIL_INFOCLASS_ALL, RIL_INFOCLASS_PADACCESS, RIL_INFOCLASS_SMS, ntddrilapitypes/RIL_INFOCLASS_PACKETACCESS, ntddrilapitypes/RIL_INFOCLASS_ALL, ntddrilapitypes/RIL_INFOCLASS_DATACIRCUITSYNC, ntddrilapitypes/RIL_INFOCLASS_DATACIRCUITASYNC, ntddrilapitypes/RIL_INFOCLASS_DATA, ntddrilapitypes/RIL_INFOCLASS_FAX, ntddrilapitypes/RIL_INFOCLASS_VOICE, RIL_INFOCLASS_FAX, netvista.rilinfoclass, RIL_INFOCLASS_VOICE, ntddrilapitypes/RIL_INFOCLASS_SMS, RIL_INFOCLASS_DATACIRCUITASYNC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddrilapitypes.h
req.include-header: 
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
-	ntddrilapitypes.h
apiname:
-	RILINFOCLASS
product: Windows
targetos: Windows
req.typenames: RILINFOCLASS
---

# RILINFOCLASS enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef enum _RILINFOCLASS { 
  RIL_INFOCLASS_VOICE,
  RIL_INFOCLASS_DATA,
  RIL_INFOCLASS_FAX,
  RIL_INFOCLASS_SMS,
  RIL_INFOCLASS_DATACIRCUITSYNC,
  RIL_INFOCLASS_DATACIRCUITASYNC,
  RIL_INFOCLASS_PACKETACCESS,
  RIL_INFOCLASS_PADACCESS,
  RIL_INFOCLASS_ALL
} RILINFOCLASS;
````


## -enum-fields




### -field RIL_INFOCLASS_NONE


### -field RIL_INFOCLASS_VOICE


### -field RIL_INFOCLASS_DATA


### -field RIL_INFOCLASS_FAX


### -field RIL_INFOCLASS_SMS


### -field RIL_INFOCLASS_DATACIRCUITSYNC


### -field RIL_INFOCLASS_DATACIRCUITASYNC


### -field RIL_INFOCLASS_PACKETACCESS


### -field RIL_INFOCLASS_PADACCESS


### -field RIL_INFOCLASS_ALL

