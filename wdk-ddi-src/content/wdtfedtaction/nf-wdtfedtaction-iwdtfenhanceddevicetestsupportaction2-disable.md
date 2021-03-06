---
UID: NF:wdtfedtaction.IWDTFEnhancedDeviceTestSupportAction2.Disable
title: IWDTFEnhancedDeviceTestSupportAction2::Disable method
author: windows-driver-content
description: Disables the Enhanced Device Test (EDT) filter driver on the target device.
old-location: dtf\iwdtfenhanceddevicetestsupportaction2_disable.htm
old-project: dtf
ms.assetid: cf67d391-8c73-43d7-aab3-57837c78dbc4
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IWDTFEnhancedDeviceTestSupportAction2 interface [Windows Device Testing Framework], Disable method, wdtfedtaction/IWDTFEnhancedDeviceTestSupportAction2::Disable, Disable method [Windows Device Testing Framework], Microsoft.WDTF.IWDTFEnhancedDeviceTestSupportAction2.Disable, IWDTFEnhancedDeviceTestSupportAction2::Disable, Microsoft::WDTF::IWDTFEnhancedDeviceTestSupportAction2::Disable, Disable method [Windows Device Testing Framework], IWDTFEnhancedDeviceTestSupportAction2 interface, Disable, IWDTFEnhancedDeviceTestSupportAction2, dtf.iwdtfenhanceddevicetestsupportaction2_disable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfedtaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFEDTAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverEDTAction.Interop.dll
req.type-library: 
req.lib: wdtfedtaction.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTFDriverEDTAction.Interop.dll
apiname:
-	IWDTFEnhancedDeviceTestSupportAction2.Disable
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFEnhancedDeviceTestSupportAction2::Disable method


## -description


Disables the Enhanced Device Test (EDT) filter driver on the target device.


## -syntax


````
HRESULT Disable(
  [out, retval] VARIANT_BOOL *pbRebootRequired
);
````


## -parameters




### -param pbRebootRequired [out, retval]

True if the operation requires a restart to complete; otherwise, false.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\wdtfedtaction\nn-wdtfedtaction-iwdtfenhanceddevicetestsupportaction2.md">IWDTFEnhancedDeviceTestSupportAction2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFEnhancedDeviceTestSupportAction2::Disable method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

