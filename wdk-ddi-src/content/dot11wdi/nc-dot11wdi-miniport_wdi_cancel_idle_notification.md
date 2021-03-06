---
UID: NC:dot11wdi.MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION
title: MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION
author: windows-driver-content
description: NDIS calls the MiniportWdiCancelIdleNotification handler function to notify the WDI miniport driver that NDIS has detected activity on the suspended network adapter.
old-location: netvista\miniportwdicancelidlenotification.htm
old-project: netvista
ms.assetid: 4C52E367-2E75-47EC-8743-F3FA2EEE25F8
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.miniportwdicancelidlenotification, MiniportWdiCancelIdleNotification callback function [Network Drivers Starting with Windows Vista], MiniportWdiCancelIdleNotification, MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION, MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION, dot11wdi/MiniportWdiCancelIdleNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dot11wdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
-	UserDefined
apilocation:
-	dot11wdi.h
apiname:
-	MiniportWdiCancelIdleNotification
product: Windows
targetos: Windows
req.typenames: "*PSYNTH_STATS, SYNTH_STATS"
---

# MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION callback


## -description


NDIS calls the MiniportWdiCancelIdleNotification handler function to notify the WDI miniport driver that NDIS has detected activity on the suspended network adapter. Because of this, NDIS cancels the idle notification so that the network adapter can be transitioned to a full-power state.

This is a WDI miniport handler inside <a href="..\dot11wdi\ns-dot11wdi-_ndis_miniport_driver_wdi_characteristics.md">NDIS_MINIPORT_DRIVER_WDI_CHARACTERISTICS</a>.
<div class="alert"><b>Note</b>  You must declare the function by using the <b>MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION</b> type. For more
   information, see the following Examples section.</div><div> </div>

## -prototype


````
MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION MiniportWdiCancelIdleNotification;

VOID MiniportWdiCancelIdleNotification(
  _In_ NDIS_HANDLE MiniportAdapterContext
)
{ ... }
````


## -parameters




### -param MiniportAdapterContext [in]

The handle to the context area that the miniport driver allocated.


## -returns



This callback function does not return a value.




## -see-also

<a href="..\dot11wdi\ns-dot11wdi-_ndis_miniport_driver_wdi_characteristics.md">NDIS_MINIPORT_DRIVER_WDI_CHARACTERISTICS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20MINIPORT_WDI_CANCEL_IDLE_NOTIFICATION callback function%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

