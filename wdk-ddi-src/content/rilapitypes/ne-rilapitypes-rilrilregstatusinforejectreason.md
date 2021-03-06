---
UID: NE:rilapitypes.RILRILREGSTATUSINFOREJECTREASON
title: RILRILREGSTATUSINFOREJECTREASON
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilrilregstatusinforejectreason_2.htm
old-project: netvista
ms.assetid: 5cc78c46-f426-470c-8f08-bbcf5e8fa1b8
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: rilapitypes/RIL_REGREJECTREASON_IMSIUNK_VLR, RIL_REGREJECTREASON_NETWORKFAILURE, rilapitypes/RIL_REGREJECTREASON_PLMN_NOTALLOWED, RIL_REGREJECTREASON_CONGESTION, RIL_REGREJECTREASON_LOCAREA_NOTALLOWED, RIL_REGREJECTREASON_IMSIUNK_VLR, rilapitypes/RIL_REGREJECTREASON_MACFAILURE, rilapitypes/RIL_REGREJECTREASON_CONGESTION, RIL_REGREJECTREASON_SVCOPT_NOTSUPPORTED, rilapitypes/RILRILREGSTATUSINFOREJECTREASON, RIL_REGREJECTREASON_ROAMING_NOTALLOWED, RIL_REGREJECTREASON_MACFAILURE, netvista.rilrilregstatusinforejectreason_2, RIL_REGREJECTREASON_ILLEGAL_ME, rilapitypes/RIL_REGREJECTREASON_ILLEGAL_ME, rilapitypes/RIL_REGREJECTREASON_SVCOPT_NOTSUPPORTED, RIL_REGREJECTREASON_SVCOPT_OUTOFORDER, RIL_REGREJECTREASON_NOSUITABLECELL, rilapitypes/RIL_REGREJECTREASON_IMSI_NOTACCEPTED, rilapitypes/RIL_REGREJECTREASON_NOSUITABLECELL, RILRILREGSTATUSINFOREJECTREASON enumeration [Network Drivers Starting with Windows Vista], RIL_REGREJECTREASON_ILLEGAL_MS, RIL_REGREJECTREASON_IMSIUNK_HLR, rilapitypes/RIL_REGREJECTREASON_GSMAUTH_NOTACCEPTED, rilapitypes/RIL_REGREJECTREASON_CSG_NOTAUTHORIZED, RIL_REGREJECTREASON_REQSVCOPT_NOTSUBSCRIBED, rilapitypes/RIL_REGREJECTREASON_SVCOPT_OUTOFORDER, RIL_REGREJECTREASON_PLMN_NOTALLOWED, RILRILREGSTATUSINFOREJECTREASON, RIL_REGREJECTREASON_CSG_NOTAUTHORIZED, rilapitypes/RIL_REGREJECTREASON_IMSIUNK_HLR, rilapitypes/RIL_REGREJECTREASON_ILLEGAL_MS, RIL_REGREJECTREASON_GSMAUTH_NOTACCEPTED, rilapitypes/RIL_REGREJECTREASON_SYNCHFAILURE, RIL_REGREJECTREASON_IMSI_NOTACCEPTED, rilapitypes/RIL_REGREJECTREASON_NETWORKFAILURE, rilapitypes/RIL_REGREJECTREASON_LOCAREA_NOTALLOWED, RIL_REGREJECTREASON_SYNCHFAILURE, rilapitypes/RIL_REGREJECTREASON_ROAMING_NOTALLOWED, rilapitypes/RIL_REGREJECTREASON_REQSVCOPT_NOTSUBSCRIBED
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
-	RILRILREGSTATUSINFOREJECTREASON
product: Windows
targetos: Windows
req.typenames: RILRILREGSTATUSINFOREJECTREASON
req.product: Windows 10 or later.
---

# RILRILREGSTATUSINFOREJECTREASON enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef enum _RILRILREGSTATUSINFOREJECTREASON { 
  RIL_REGREJECTREASON_IMSIUNK_HLR,
  RIL_REGREJECTREASON_ILLEGAL_MS,
  RIL_REGREJECTREASON_IMSIUNK_VLR,
  RIL_REGREJECTREASON_IMSI_NOTACCEPTED,
  RIL_REGREJECTREASON_ILLEGAL_ME,
  RIL_REGREJECTREASON_PLMN_NOTALLOWED,
  RIL_REGREJECTREASON_LOCAREA_NOTALLOWED,
  RIL_REGREJECTREASON_ROAMING_NOTALLOWED,
  RIL_REGREJECTREASON_NOSUITABLECELL,
  RIL_REGREJECTREASON_NETWORKFAILURE,
  RIL_REGREJECTREASON_MACFAILURE,
  RIL_REGREJECTREASON_SYNCHFAILURE,
  RIL_REGREJECTREASON_CONGESTION,
  RIL_REGREJECTREASON_GSMAUTH_NOTACCEPTED,
  RIL_REGREJECTREASON_CSG_NOTAUTHORIZED,
  RIL_REGREJECTREASON_SVCOPT_NOTSUPPORTED,
  RIL_REGREJECTREASON_REQSVCOPT_NOTSUBSCRIBED,
  RIL_REGREJECTREASON_SVCOPT_OUTOFORDER
} RILRILREGSTATUSINFOREJECTREASON;
````


## -enum-fields




### -field RIL_REGREJECTREASON_NULL


### -field RIL_REGREJECTREASON_IMSIUNK_HLR


### -field RIL_REGREJECTREASON_ILLEGAL_MS


### -field RIL_REGREJECTREASON_IMSIUNK_VLR


### -field RIL_REGREJECTREASON_IMSI_NOTACCEPTED


### -field RIL_REGREJECTREASON_ILLEGAL_ME


### -field RIL_REGREJECTREASON_PLMN_NOTALLOWED


### -field RIL_REGREJECTREASON_LOCAREA_NOTALLOWED


### -field RIL_REGREJECTREASON_ROAMING_NOTALLOWED


### -field RIL_REGREJECTREASON_NOSUITABLECELL


### -field RIL_REGREJECTREASON_NETWORKFAILURE


### -field RIL_REGREJECTREASON_MACFAILURE


### -field RIL_REGREJECTREASON_SYNCHFAILURE


### -field RIL_REGREJECTREASON_CONGESTION


### -field RIL_REGREJECTREASON_GSMAUTH_NOTACCEPTED


### -field RIL_REGREJECTREASON_CSG_NOTAUTHORIZED


### -field RIL_REGREJECTREASON_SVCOPT_NOTSUPPORTED


### -field RIL_REGREJECTREASON_REQSVCOPT_NOTSUBSCRIBED


### -field RIL_REGREJECTREASON_SVCOPT_OUTOFORDER

