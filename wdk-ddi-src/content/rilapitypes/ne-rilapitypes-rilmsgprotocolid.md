---
UID: NE:rilapitypes.RILMSGPROTOCOLID
title: RILMSGPROTOCOLID
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilmsgprotocolid_2.htm
old-project: netvista
ms.assetid: a4dc4bc4-f636-46be-b99c-12d2bf4a577f
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: rilapitypes/RIL_MSGPROTOCOL_ERMES, RIL_MSGPROTOCOL_TELEX, RIL_MSGPROTOCOL_TELETEX_ISDN, netvista.rilmsgprotocolid_2, rilapitypes/RILMSGPROTOCOLID, rilapitypes/RIL_MSGPROTOCOL_RSM_TYPE5, rilapitypes/RIL_MSGPROTOCOL_GSMSTATION, rilapitypes/RIL_MSGPROTOCOL_SCSPECIFIC7, RIL_MSGPROTOCOL_TELEFAX_GROUP4, RIL_MSGPROTOCOL_DEPERSONALIZATION, RIL_MSGPROTOCOL_SCSPECIFIC3, RIL_MSGPROTOCOL_RSM_TYPE4, RILMSGPROTOCOLID, rilapitypes/RIL_MSGPROTOCOL_DEPERSONALIZATION, rilapitypes/RIL_MSGPROTOCOL_SM_TYPE0, rilapitypes/RIL_MSGPROTOCOL_SCSPECIFIC3, RIL_MSGPROTOCOL_RSM_TYPE5, rilapitypes/RIL_MSGPROTOCOL_TELEFAX_GROUP3, RIL_MSGPROTOCOL_X400, RIL_MSGPROTOCOL_RSM_TYPE7, rilapitypes/RIL_MSGPROTOCOL_RSM_TYPE6, rilapitypes/RIL_MSGPROTOCOL_UCI, RIL_MSGPROTOCOL_TELETEX_CSPDN, RIL_MSGPROTOCOL_TELEFAX_GROUP3, RIL_MSGPROTOCOL_UCI, RIL_MSGPROTOCOL_MAX, RIL_MSGPROTOCOL_RSM_TYPE1, rilapitypes/RIL_MSGPROTOCOL_VOICEPHONE, rilapitypes/RIL_MSGPROTOCOL_PAGING, RIL_MSGPROTOCOL_MSGHANDLING, rilapitypes/RIL_MSGPROTOCOL_RSM_TYPE2, RIL_MSGPROTOCOL_RSM_TYPE2, rilapitypes/RIL_MSGPROTOCOL_IMPLICIT, rilapitypes/RIL_MSGPROTOCOL_TELETEX_PSPDN, rilapitypes/RIL_MSGPROTOCOL_MAX, RIL_MSGPROTOCOL_SCSPECIFIC5, rilapitypes/RIL_MSGPROTOCOL_ME_DOWNLOAD, rilapitypes/RIL_MSGPROTOCOL_MSGHANDLING, RILMSGPROTOCOLID enumeration [Network Drivers Starting with Windows Vista], RIL_MSGPROTOCOL_VIDEOTEX, rilapitypes/RIL_MSGPROTOCOL_SCSPECIFIC5, RIL_MSGPROTOCOL_EMAIL, RIL_MSGPROTOCOL_SM_TYPE0, rilapitypes/RIL_MSGPROTOCOL_RSM_TYPE7, rilapitypes/RIL_MSGPROTOCOL_EMAIL, RIL_MSGPROTOCOL_SCSPECIFIC4, rilapitypes/RIL_MSGPROTOCOL_RSM_TYPE3, rilapitypes/RIL_MSGPROTOCOL_RETURNCALL, RIL_MSGPROTOCOL_ME_DOWNLOAD, rilapitypes/RIL_MSGPROTOCOL_SMETOSME, RIL_MSGPROTOCOL_SCSPECIFIC6, rilapitypes/RIL_MSGPROTOCOL_TELETEX, RIL_MSGPROTOCOL_TELETEX_PSPDN, RIL_MSGPROTOCOL_ERMES, rilapitypes/RIL_MSGPROTOCOL_VIDEOTEX, rilapitypes/RIL_MSGPROTOCOL_TELETEX_ISDN, rilapitypes/RIL_MSGPROTOCOL_X400, rilapitypes/RIL_MSGPROTOCOL_SCSPECIFIC2, RIL_MSGPROTOCOL_RETURNCALL, RIL_MSGPROTOCOL_TELETEX_PSTN, rilapitypes/RIL_MSGPROTOCOL_TELETEX_CSPDN, RIL_MSGPROTOCOL_UICC_DOWNLOAD, rilapitypes/RIL_MSGPROTOCOL_UICC_DOWNLOAD, rilapitypes/RIL_MSGPROTOCOL_TELEFAX_GROUP4, RIL_MSGPROTOCOL_RSM_TYPE3, RIL_MSGPROTOCOL_SCSPECIFIC7, rilapitypes/RIL_MSGPROTOCOL_SCSPECIFIC1, rilapitypes/RIL_MSGPROTOCOL_RSM_TYPE1, RIL_MSGPROTOCOL_TELETEX, rilapitypes/RIL_MSGPROTOCOL_TELEX, RIL_MSGPROTOCOL_SCSPECIFIC1, rilapitypes/RIL_MSGPROTOCOL_SCSPECIFIC6, rilapitypes/RIL_MSGPROTOCOL_RSM_TYPE4, rilapitypes/RIL_MSGPROTOCOL_SCSPECIFIC4, RIL_MSGPROTOCOL_VOICEPHONE, RIL_MSGPROTOCOL_PAGING, RIL_MSGPROTOCOL_IMPLICIT, RIL_MSGPROTOCOL_SMETOSME, RIL_MSGPROTOCOL_RSM_TYPE6, rilapitypes/RIL_MSGPROTOCOL_TELETEX_PSTN, RIL_MSGPROTOCOL_GSMSTATION, RIL_MSGPROTOCOL_SCSPECIFIC2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: rilapitypes.h
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	rilapitypes.h
apiname:
-	RILMSGPROTOCOLID
product: Windows
targetos: Windows
req.typenames: RILMSGPROTOCOLID
req.product: Windows 10 or later.
---

# RILMSGPROTOCOLID enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef enum _RILMSGPROTOCOLID { 
  RIL_MSGPROTOCOL_SMETOSME,
  RIL_MSGPROTOCOL_IMPLICIT,
  RIL_MSGPROTOCOL_TELEX,
  RIL_MSGPROTOCOL_TELEFAX_GROUP3,
  RIL_MSGPROTOCOL_TELEFAX_GROUP4,
  RIL_MSGPROTOCOL_VOICEPHONE,
  RIL_MSGPROTOCOL_ERMES,
  RIL_MSGPROTOCOL_PAGING,
  RIL_MSGPROTOCOL_VIDEOTEX,
  RIL_MSGPROTOCOL_TELETEX,
  RIL_MSGPROTOCOL_TELETEX_PSPDN,
  RIL_MSGPROTOCOL_TELETEX_CSPDN,
  RIL_MSGPROTOCOL_TELETEX_PSTN,
  RIL_MSGPROTOCOL_TELETEX_ISDN,
  RIL_MSGPROTOCOL_UCI,
  RIL_MSGPROTOCOL_MSGHANDLING,
  RIL_MSGPROTOCOL_X400,
  RIL_MSGPROTOCOL_EMAIL,
  RIL_MSGPROTOCOL_SCSPECIFIC1,
  RIL_MSGPROTOCOL_SCSPECIFIC2,
  RIL_MSGPROTOCOL_SCSPECIFIC3,
  RIL_MSGPROTOCOL_SCSPECIFIC4,
  RIL_MSGPROTOCOL_SCSPECIFIC5,
  RIL_MSGPROTOCOL_SCSPECIFIC6,
  RIL_MSGPROTOCOL_SCSPECIFIC7,
  RIL_MSGPROTOCOL_GSMSTATION,
  RIL_MSGPROTOCOL_SM_TYPE0,
  RIL_MSGPROTOCOL_RSM_TYPE1,
  RIL_MSGPROTOCOL_RSM_TYPE2,
  RIL_MSGPROTOCOL_RSM_TYPE3,
  RIL_MSGPROTOCOL_RSM_TYPE4,
  RIL_MSGPROTOCOL_RSM_TYPE5,
  RIL_MSGPROTOCOL_RSM_TYPE6,
  RIL_MSGPROTOCOL_RSM_TYPE7,
  RIL_MSGPROTOCOL_RETURNCALL,
  RIL_MSGPROTOCOL_ME_DOWNLOAD,
  RIL_MSGPROTOCOL_DEPERSONALIZATION,
  RIL_MSGPROTOCOL_UICC_DOWNLOAD,
  RIL_MSGPROTOCOL_MAX
} RILMSGPROTOCOLID;
````


## -enum-fields




### -field RIL_MSGPROTOCOL_UNKNOWN


### -field RIL_MSGPROTOCOL_SMETOSME


### -field RIL_MSGPROTOCOL_IMPLICIT


### -field RIL_MSGPROTOCOL_TELEX


### -field RIL_MSGPROTOCOL_TELEFAX_GROUP3


### -field RIL_MSGPROTOCOL_TELEFAX_GROUP4


### -field RIL_MSGPROTOCOL_VOICEPHONE


### -field RIL_MSGPROTOCOL_ERMES


### -field RIL_MSGPROTOCOL_PAGING


### -field RIL_MSGPROTOCOL_VIDEOTEX


### -field RIL_MSGPROTOCOL_TELETEX


### -field RIL_MSGPROTOCOL_TELETEX_PSPDN


### -field RIL_MSGPROTOCOL_TELETEX_CSPDN


### -field RIL_MSGPROTOCOL_TELETEX_PSTN


### -field RIL_MSGPROTOCOL_TELETEX_ISDN


### -field RIL_MSGPROTOCOL_UCI


### -field RIL_MSGPROTOCOL_MSGHANDLING


### -field RIL_MSGPROTOCOL_X400


### -field RIL_MSGPROTOCOL_EMAIL


### -field RIL_MSGPROTOCOL_SCSPECIFIC1


### -field RIL_MSGPROTOCOL_SCSPECIFIC2


### -field RIL_MSGPROTOCOL_SCSPECIFIC3


### -field RIL_MSGPROTOCOL_SCSPECIFIC4


### -field RIL_MSGPROTOCOL_SCSPECIFIC5


### -field RIL_MSGPROTOCOL_SCSPECIFIC6


### -field RIL_MSGPROTOCOL_SCSPECIFIC7


### -field RIL_MSGPROTOCOL_GSMSTATION


### -field RIL_MSGPROTOCOL_SM_TYPE0


### -field RIL_MSGPROTOCOL_RSM_TYPE1


### -field RIL_MSGPROTOCOL_RSM_TYPE2


### -field RIL_MSGPROTOCOL_RSM_TYPE3


### -field RIL_MSGPROTOCOL_RSM_TYPE4


### -field RIL_MSGPROTOCOL_RSM_TYPE5


### -field RIL_MSGPROTOCOL_RSM_TYPE6


### -field RIL_MSGPROTOCOL_RSM_TYPE7


### -field RIL_MSGPROTOCOL_RETURNCALL


### -field RIL_MSGPROTOCOL_ME_DOWNLOAD


### -field RIL_MSGPROTOCOL_DEPERSONALIZATION


### -field RIL_MSGPROTOCOL_UICC_DOWNLOAD


### -field RIL_MSGPROTOCOL_MAX

