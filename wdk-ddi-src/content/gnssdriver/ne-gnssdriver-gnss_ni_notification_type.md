---
UID: NE:gnssdriver.GNSS_NI_NOTIFICATION_TYPE
title: GNSS_NI_NOTIFICATION_TYPE
author: windows-driver-content
description: GNSS_NI_NOTIFICATION_TYPE enumerates network-initialized (NI) notification types.
old-location: sensors\gnss_ni_notification_type.htm
old-project: sensors
ms.assetid: EC5FB722-F182-44A5-944C-ED81E43492AE
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: gnssdriver/GNSS_NI_PrivacyOverride, GNSS_NI_PrivacyOverride, gnssdriver/GNSS_NI_NoNotifyNoVerify, gnssdriver/GNSS_NI_NotifyOnly, GNSS_NI_NotifyVerifyDefaultAllow, gnssdriver/GNSS_NI_NotifyVerifyDefaultAllow, GNSS_NI_NotifyVerifyDefaultNotAllow, gnssdriver/GNSS_NI_NOTIFICATION_TYPE, GNSS_NI_NotifyOnly, GNSS_NI_NOTIFICATION_TYPE enumeration [Sensor Devices], GNSS_NI_NoNotifyNoVerify, GNSS_NI_NOTIFICATION_TYPE, gnssdriver/GNSS_NI_NotifyVerifyDefaultNotAllow, sensors.gnss_ni_notification_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: gnssdriver.h
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
req.irql: "<= DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	gnssdriver.h
apiname:
-	GNSS_NI_NOTIFICATION_TYPE
product: Windows
targetos: Windows
req.typenames: GNSS_NI_NOTIFICATION_TYPE
---

# GNSS_NI_NOTIFICATION_TYPE enumeration


## -description


GNSS_NI_NOTIFICATION_TYPE enumerates network-initialized (NI) notification types.


## -syntax


````
typedef enum  { 
  GNSS_NI_NoNotifyNoVerify             = 0x01,
  GNSS_NI_NotifyOnly                   = 0x02,
  GNSS_NI_NotifyVerifyDefaultAllow     = 0x03,
  GNSS_NI_NotifyVerifyDefaultNotAllow  = 0x04,
  GNSS_NI_PrivacyOverride              = 0x05
} GNSS_NI_NOTIFICATION_TYPE;
````


## -enum-fields




### -field GNSS_NI_NoNotifyNoVerify

No notification and no verification.


### -field GNSS_NI_NotifyOnly

Notification only.


### -field GNSS_NI_NotifyVerifyDefaultAllow

Notification and verification allowed on no answer.


### -field GNSS_NI_NotifyVerifyDefaultNotAllow

Notification and verification denied on no answer.


### -field GNSS_NI_PrivacyOverride

Privacy override.

This is used for preventing notification and verification without leaving any traces of a performed position fix or position fix attempt.

