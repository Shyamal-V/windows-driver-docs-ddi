---
UID: NF:wdtf.IWDTFSystemDepot2.get_WDTF
title: IWDTFSystemDepot2::get_WDTF method
author: windows-driver-content
description: Gets the main WDTF aggregation object.
old-location: dtf\iwdtfdevicedepot2_wdtf.htm
old-project: dtf
ms.assetid: 911e5f2b-bd8c-42e6-8272-a447e723e814
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IWDTFDeviceDepot2 interface [Windows Device Testing Framework], WDTF property, WDTF property [Windows Device Testing Framework], Microsoft.WDTF.IWDTFDeviceDepot2.WDTF, IWDTFDeviceDepot2, IWDTFSystemDepot2, wdtf/IWDTFDeviceDepot2::WDTF, IWDTFSystemDepot2::get_WDTF, IWDTFDeviceDepot2.WDTF, Microsoft::WDTF::IWDTFDeviceDepot2::WDTF, dtf.iwdtfdevicedepot2_wdtf, IWDTFDeviceDepot2::get_WDTF, wdtf/IWDTFDeviceDepot2::get_WDTF, get_WDTF, WDTF property [Windows Device Testing Framework], IWDTFDeviceDepot2 interface
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
-	IWDTFDeviceDepot2.WDTF
-	IWDTFDeviceDepot2.get_WDTF
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFSystemDepot2::get_WDTF method


## -description


Gets the main WDTF aggregation object.

This property is read-only.


## -syntax


````
HRESULT get_WDTF(
  [out, retval] IWDTF2 **ppWDTF
);
````


## -parameters


## -see-also

<a href="..\wdtf\nn-wdtf-iwdtfdevicedepot2.md">IWDTFDeviceDepot2</a>



<a href="..\wdtf\nn-wdtf-iwdtf2.md">IWDTF2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFDeviceDepot2::WDTF property%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

