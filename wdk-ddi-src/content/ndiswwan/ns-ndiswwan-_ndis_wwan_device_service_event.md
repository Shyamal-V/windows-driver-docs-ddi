---
UID: NS:ndiswwan._NDIS_WWAN_DEVICE_SERVICE_EVENT
title: "_NDIS_WWAN_DEVICE_SERVICE_EVENT"
author: windows-driver-content
description: The NDIS_WWAN_DEVICE_SERVICE_EVENT structure describes unsolicited device service data that were not initiated by commands from Windows.
old-location: netvista\ndis_wwan_device_service_event.htm
old-project: netvista
ms.assetid: 43205AA6-2B1A-4D04-9AF8-E0EB53253F5B
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: PNDIS_WWAN_DEVICE_SERVICE_EVENT structure pointer [Network Drivers Starting with Windows Vista], ndiswwan/PNDIS_WWAN_DEVICE_SERVICE_EVENT, NDIS_WWAN_DEVICE_SERVICE_EVENT, PNDIS_WWAN_DEVICE_SERVICE_EVENT, *PNDIS_WWAN_DEVICE_SERVICE_EVENT, NDIS_WWAN_DEVICE_SERVICE_EVENT structure [Network Drivers Starting with Windows Vista], ndiswwan/NDIS_WWAN_DEVICE_SERVICE_EVENT, _NDIS_WWAN_DEVICE_SERVICE_EVENT, netvista.ndis_wwan_device_service_event
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ndiswwan.h
req.include-header: Ndiswwan.h
req.target-type: Windows
req.target-min-winverclnt: Versions:\_Supported in Windows 8 and later versions of Windows.
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
req.irql: PASSIVE_LEVEL
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	ndiswwan.h
apiname:
-	NDIS_WWAN_DEVICE_SERVICE_EVENT
product: Windows
targetos: Windows
req.typenames: NDIS_WWAN_DEVICE_SERVICE_EVENT, *PNDIS_WWAN_DEVICE_SERVICE_EVENT
---

# _NDIS_WWAN_DEVICE_SERVICE_EVENT structure


## -description


The NDIS_WWAN_DEVICE_SERVICE_EVENT structure describes unsolicited device service data that were not initiated by commands from Windows.


## -syntax


````
typedef struct _NDIS_WWAN_DEVICE_SERVICE_EVENT {
  NDIS_OBJECT_HEADER        Header;
  WWAN_DEVICE_SERVICE_EVENT EventData;
} NDIS_WWAN_DEVICE_SERVICE_EVENT, *PNDIS_WWAN_DEVICE_SERVICE_EVENT;
````


## -struct-fields




### -field Header

The header with type, revision, and size information about the NDIS_WWAN_DEVICE_SERVICE_EVENT structure. The MB
     Service sets the header with the values that are shown in the following table when it sends the data
     structure to the miniport driver for 
     <i>set</i> operations. Miniport drivers must set the header with the same values when they send the data
     structure to the MB service.
     

<table>
<tr>
<th>Header submember</th>
<th>Value</th>
</tr>
<tr>
<td>
Type

</td>
<td>
NDIS_OBJECT_TYPE_DEFAULT

</td>
</tr>
<tr>
<td>
Revision

</td>
<td>
NDIS_WWAN_DEVICE_SERVICE_EVENT_REVISION_1

</td>
</tr>
<tr>
<td>
Size

</td>
<td>
sizeof(NDIS_WWAN_DEVICE_SERVICE_EVENT)

</td>
</tr>
</table>
 

For more information about these members, see 
     <a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a>.


### -field Event

 




#### - EventData

The information from the event.


## -see-also

<a href="..\wwan\ns-wwan-_wwan_device_service_event.md">WWAN_DEVICE_SERVICE_EVENT</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_WWAN_DEVICE_SERVICE_EVENT structure%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

