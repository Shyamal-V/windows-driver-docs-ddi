---
UID: NE:bthddi._INDICATION_CODE
title: "_INDICATION_CODE"
author: windows-driver-content
description: The INDICATION_CODE enumeration type indicates to a profile driver what type of L2CAP event has occurred.
old-location: bltooth\indication_code.htm
old-project: bltooth
ms.assetid: 7fc374e3-ca5b-476d-bc44-afb28ecf9920
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: bthddi/IndicationUnpairDevice, bthddi/IndicationPairDevice, bthddi/INDICATION_CODE, IndicationRemoteDisconnect, _INDICATION_CODE, bthddi/IndicationReleaseReference, bthddi/IndicationAddReference, bthddi/IndicationRemoteDisconnect, IndicationUnpairDevice, bthddi/IndicationRemoteConnect, bthddi/IndicationRecvPacket, bthddi/IndicationRemoteConfigResponse, bthddi/IndicationRemoteConfigRequest, IndicationRemoteConfigResponse, IndicationPairDevice, IndicationRemoteConfigRequest, INDICATION_CODE enumeration [Bluetooth Devices], IndicationRemoteConnectLE, IndicationRemoteConnect, bthddi/IndicationFreeExtraOptions, bltooth.indication_code, PINDICATION_CODE, bth_enums_89c3fcea-8183-4227-b3fb-4e18c3612326.xml, bthddi/PINDICATION_CODE, IndicationAddReference, IndicationReleaseReference, bthddi/IndicationUnpersonalizeDevice, IndicationRecvPacket, IndicationUnpersonalizeDevice, bthddi/IndicationRemoteConnectLE, INDICATION_CODE, PINDICATION_CODE enumeration pointer [Bluetooth Devices], *PINDICATION_CODE, IndicationFreeExtraOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: bthddi.h
req.include-header: Bthddi.h
req.target-type: Windows
req.target-min-winverclnt: Versions:\_Supported in Windows Vista, and later.
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
req.irql: Developers should code this function to operate at either IRQL = DISPATCH_LEVEL (if the callback   function does not access paged memory), or IRQL = PASSIVE_LEVEL (if the callback function must access   paged memory)
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	bthddi.h
apiname:
-	INDICATION_CODE
product: Windows
targetos: Windows
req.typenames: "*PINDICATION_CODE, INDICATION_CODE"
---

# _INDICATION_CODE enumeration


## -description


The INDICATION_CODE enumeration type indicates to a profile driver what type of L2CAP event has
  occurred.


## -syntax


````
typedef enum _INDICATION_CODE { 
  IndicationAddReference          = 0,
  IndicationReleaseReference,
  IndicationRemoteConnect,
  IndicationRemoteDisconnect,
  IndicationRemoteConfigRequest   = 4,
  IndicationRemoteConfigResponse,
  IndicationFreeExtraOptions      = 6,
  IndicationRecvPacket,
  IndicationPairDevice,
  IndicationUnpairDevice          = 9,
  IndicationUnpersonalizeDevice,
  IndicationRemoteConnectLE
} INDICATION_CODE, *PINDICATION_CODE;
````


## -enum-fields




### -field IndicationAddReference

Indicates to a profile driver to add a reference to its device object because it may be called at
     any time.


### -field IndicationReleaseReference

Indicates to a profile driver to release a reference to its device object and that it will no
     longer be called.


### -field IndicationRemoteConnect

Indicates to a server profile driver that a remote device is connecting to the PSM that the
     profile driver registered earlier. Profile drivers accept or reject this request by 
     <a href="https://msdn.microsoft.com/53a692e7-9c71-4dca-9331-32ac97b94179">building and sending</a> a 
     <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff536616">
     BRB_L2CA_OPEN_CHANNEL_RESPONSE</a> request. When this indication code is passed, the profile driver
     should use the parameters that are passed to it in the 
     <b>Connect</b> member of the 
     <a href="..\bthddi\ns-bthddi-_indication_parameters.md">
     INDICATION_PARAMETERS</a> structure.


### -field IndicationRemoteDisconnect

Indicates to a registered profile driver that a remote device disconnecting from the local radio.
     When this indication code is passed, the profile driver should use the parameters that are passed to it
     in the 
     <b>Disconnect</b> member of the INDICATION_PARAMETERS structure.


### -field IndicationRemoteConfigRequest

Indicates to a client profile driver that a remote device is performing a configuration request.
     When this indication code is passed, the profile driver should use the parameters that are passed to it
     in the 
     <b>ConfigRequest</b> member of the INDICATION_PARAMETERS structure.


### -field IndicationRemoteConfigResponse

Indicates to a client profile driver that a remote device is responding to a configuration
     request. When this indication code is passed, the profile driver should use the parameters that are
     passed to it in the 
     <b>ConfigResponse</b> member of the INDICATION_PARAMETERS structure.


### -field IndicationFreeExtraOptions

Reserved for future use. Do not use.


### -field IndicationRecvPacket

Indicates to a registered profile driver that a packet has been received on the specified PSM. The
     profile driver can use this event to determine when it is necessary to issue a read
     BRB_L2CA_ACL_TRANSFTER BRB. Profile drivers that need to read from the remote device can also ignore
     this notification and keep a read BRB pending at all times. When this indication code is passed, the
     profile driver should use the parameters that are passed to it in the 
     <b>RecvPacket</b> member of the 
     <a href="..\bthddi\ns-bthddi-_indication_parameters.md">
     INDICATION_PARAMETERS</a> structure.


### -field IndicationPairDevice

Indicates to a registered driver that the local radio has bonded to a specific remote
     radio.


### -field IndicationUnpairDevice

Indicates to a registered driver that the local radio is no longer bonded to a specific remote
     radio.


### -field IndicationUnpersonalizeDevice

Indicates to a registered driver that the specified remote radio has been removed from the list of
     personal devices.


### -field IndicationRemoteConnectLE

Indicates to a server profile driver that a low energy (LE) remote device is connecting to the PSM that the
     profile driver registered earlier. Profile drivers accept or reject this request by 
     <a href="https://msdn.microsoft.com/53a692e7-9c71-4dca-9331-32ac97b94179">building and sending</a> a 
     <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff536616">
     BRB_L2CA_OPEN_CHANNEL_RESPONSE</a> request. When this indication code is passed, the profile driver
     should use the parameters that are passed to it in the 
     <b>Connect</b> member of the 
     <a href="..\bthddi\ns-bthddi-_indication_parameters.md">
     INDICATION_PARAMETERS</a> structure. This value is present in Windows 8 and later versions of Windows.


## -remarks



A value from this enumeration is passed to a profile driver's 
    <a href="..\bthddi\nc-bthddi-pfnbthport_indication_callback.md">L2CAP Callback Function</a> to notify
    it of an event.




## -see-also

<a href="..\bthddi\ns-bthddi-_indication_parameters.md">INDICATION_PARAMETERS</a>



<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff536618">BRB_L2CA_REGISTER_SERVER</a>



<a href="..\bthddi\nc-bthddi-pfnbthport_indication_callback.md">L2CAP Callback Function</a>



<a href="..\bthioctl\ni-bthioctl-ioctl_internal_bth_submit_brb.md">IOCTL_INTERNAL_BTH_SUBMIT_BRB</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [bltooth\bltooth]:%20INDICATION_CODE enumeration%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

