---
UID: NE:netdma._NET_DMA_PNP_NOTIFICATION_CODE
title: "_NET_DMA_PNP_NOTIFICATION_CODE"
author: windows-driver-content
description: The NET_DMA_PNP_NOTIFICATION_CODE enumeration identifies the type of a NetDMA Plug and Play (PnP) event.
old-location: netvista\net_dma_pnp_notification_code.htm
old-project: netvista
ms.assetid: 1c9c09ae-5b7a-4482-8f6b-1ad5ede5b3f5
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netdma/NetDmaNotificationProviderArrival, netvista.net_dma_pnp_notification_code, NetDmaNotificationMax, netdma/NetDmaNotificationChannelArrival, NET_DMA_PNP_NOTIFICATION_CODE, NetDmaNotificationProviderPowerUp, netdma/PNET_DMA_PNP_NOTIFICATION_CODE, NetDmaNotificationChannelArrival, NetDmaNotificationProviderPowerDown, NetDmaNotificationProviderRemoval, netdma/NetDmaNotificationProviderPowerDown, PNET_DMA_PNP_NOTIFICATION_CODE enumeration pointer [Network Drivers Starting with Windows Vista], netdma/NetDmaNotificationProviderRegistered, _NET_DMA_PNP_NOTIFICATION_CODE, *PNET_DMA_PNP_NOTIFICATION_CODE, NetDmaNotificationProviderRegistered, netdma_ref_ce8373ae-1547-410d-b33e-d95eb42d649e.xml, PNET_DMA_PNP_NOTIFICATION_CODE, netdma/NET_DMA_PNP_NOTIFICATION_CODE, netdma/NetDmaNotificationProviderPowerUp, netdma/NetDmaNotificationProviderRemoval, NET_DMA_PNP_NOTIFICATION_CODE enumeration [Network Drivers Starting with Windows Vista], NetDmaNotificationProviderArrival, netdma/NetDmaNotificationMax
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: netdma.h
req.include-header: Netdma.h
req.target-type: Windows
req.target-min-winverclnt: Supported for NetDMA 2.0 and NetDMA 1.1 drivers in Windows Server 2008.
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
-	netdma.h
apiname:
-	NET_DMA_PNP_NOTIFICATION_CODE
product: Windows
targetos: Windows
req.typenames: NET_DMA_PNP_NOTIFICATION_CODE, *PNET_DMA_PNP_NOTIFICATION_CODE
---

# _NET_DMA_PNP_NOTIFICATION_CODE enumeration


## -description


<div class="alert"><b>Note</b>  The NetDMA interface is not supported in Windows 8 and later.</div><div> </div>The NET_DMA_PNP_NOTIFICATION_CODE enumeration identifies the type of a NetDMA Plug and Play (PnP)
  event.


## -syntax


````
typedef enum _NET_DMA_PNP_NOTIFICATION_CODE { 
  NetDmaNotificationProviderRegistered  = 1,
  NetDmaNotificationProviderArrival,
  NetDmaNotificationProviderRemoval,
  NetDmaNotificationChannelArrival,
  NetDmaNotificationProviderPowerDown,
  NetDmaNotificationProviderPowerUp,
  NetDmaNotificationMax
} NET_DMA_PNP_NOTIFICATION_CODE, *PNET_DMA_PNP_NOTIFICATION_CODE;
````


## -enum-fields




### -field NetDmaNotificationProviderRegistered

The NetDMA provider is registered. NetDMA uses this event in the NetDMA client interface.


### -field NetDmaNotificationProviderArrival

The NetDMA provider is available for a client to use. NetDMA uses this event in the NetDMA client
     interface.


### -field NetDmaNotificationProviderRemoval

The NetDMA provider was removed. NetDMA uses this event in the NetDMA client interface.


### -field NetDmaNotificationChannelArrival

The NetDMA channel is available for a client to use. NetDMA uses this event in the NetDMA client
     interface.


### -field NetDmaNotificationProviderPowerDown

The NetDMA provider is powering down. A NetDMA provider driver issues the 
     <b>NetDmaNotificationProviderPowerDown</b> notification before it sets the DMA provider to a low-power
     state.


### -field NetDmaNotificationProviderPowerUp

The NetDMA provider is powered up. NetDMA provider drivers issue the 
     <b>NetDmaNotificationProviderPowerUp</b> notification after the DMA provider is back to a working power
     state.


### -field NetDmaNotificationMax

The total number of supported NetDMA PnP events.


## -remarks



The NET_DMA_PNP_NOTIFICATION_CODE enumeration is used in the 
    <a href="..\netdma\ns-netdma-_net_dma_pnp_notification.md">
    NET_DMA_PNP_NOTIFICATION</a> structure.




## -see-also

<a href="..\netdma\ns-netdma-_net_dma_pnp_notification.md">NET_DMA_PNP_NOTIFICATION</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NET_DMA_PNP_NOTIFICATION_CODE enumeration%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

