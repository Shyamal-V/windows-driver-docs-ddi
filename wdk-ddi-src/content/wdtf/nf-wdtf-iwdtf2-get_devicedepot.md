---
UID: NF:wdtf.IWDTF2.get_DeviceDepot
title: IWDTF2::get_DeviceDepot method
author: windows-driver-content
description: Gets the DeviceDepot object.
old-location: dtf\iwdtf2_devicedepot.htm
old-project: dtf
ms.assetid: 9bff0ac6-149e-4a40-a6e0-a3156c3d6af5
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IWDTF2 interface [Windows Device Testing Framework], DeviceDepot property, wdtf/IWDTF2::get_DeviceDepot, get_DeviceDepot, IWDTF2::get_DeviceDepot, IWDTF2, dtf.iwdtf2_devicedepot, IWDTF2.DeviceDepot, DeviceDepot property [Windows Device Testing Framework], IWDTF2 interface, Microsoft.WDTF.IWDTF2.DeviceDepot, Microsoft::WDTF::IWDTF2::DeviceDepot, DeviceDepot property [Windows Device Testing Framework], wdtf/IWDTF2::DeviceDepot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTF.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTF.Interop.metadata_dll
req.type-library: 
req.lib: wdtf.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTF.Interop.metadata_dll.dll
apiname:
-	IWDTF2.DeviceDepot
-	IWDTF2.get_DeviceDepot
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTF2::get_DeviceDepot method


## -description


Gets the DeviceDepot object.

This property is read-only.


## -syntax


````
HRESULT get_DeviceDepot(
  [out, retval] IWDTFDeviceDepot2 **pVal
);
````


## -parameters


## -see-also

<a href="..\wdtf\nn-wdtf-iwdtfdevicedepot2.md">IWDTFDeviceDepot2</a>



<a href="..\wdtf\nn-wdtf-iwdtf2.md">IWDTF2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTF2::DeviceDepot property%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

