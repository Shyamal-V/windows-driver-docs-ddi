---
UID: NE:ntddsd.SDPROP_MEDIA_STATE
title: SDPROP_MEDIA_STATE
author: windows-driver-content
description: The SDPROP_MEDIA_STATE enumeration lists the values associated with the media states property.
old-location: sd\sdprop_media_state.htm
old-project: SD
ms.assetid: b59fd639-f2e2-4765-bcc7-01934df3a0bc
ms.author: windowsdriverdev
ms.date: 12/18/2017
ms.keywords: SDPMS_MEDIA_INSERTED, ntddsd/SDPMS_MEDIA_INSERTED, ntddsd/SDPROP_MEDIA_STATE, SD.sdprop_media_state, sd-structs_a2064f73-cec7-4703-95ec-8ab8adc0b4b2.xml, SDPMS_NO_MEDIA, SDPROP_MEDIA_STATE enumeration [Buses], SDPROP_MEDIA_STATE, ntddsd/SDPMS_NO_MEDIA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddsd.h
req.include-header: Ntddsd.h
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
-	ntddsd.h
apiname:
-	SDPROP_MEDIA_STATE
product: Windows
targetos: Windows
req.typenames: SDPROP_MEDIA_STATE
---

# SDPROP_MEDIA_STATE enumeration


## -description


The SDPROP_MEDIA_STATE enumeration lists the values associated with the media states property.


## -syntax


````
typedef enum  { 
  SDPMS_NO_MEDIA        = 0,
  SDPMS_MEDIA_INSERTED  = 1
} SDPROP_MEDIA_STATE;
````


## -enum-fields




### -field SDPMS_NO_MEDIA

Indicates that the media is not present.


### -field SDPMS_MEDIA_INSERTED

Indicates that the media is inserted.


## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537914">SdBusSubmitRequestAsync</a>



<a href="https://msdn.microsoft.com/09b30bf0-fe85-4ad5-bd3e-113ed3a093ac">SDBUS_REQUEST_PACKET</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537909">SdBusSubmitRequest</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [SD\buses]:%20SDPROP_MEDIA_STATE enumeration%20 RELEASE:%20(12/18/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

