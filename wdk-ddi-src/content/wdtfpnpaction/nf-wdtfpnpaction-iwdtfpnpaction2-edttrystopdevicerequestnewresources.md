---
UID: NF:wdtfpnpaction.IWDTFPNPAction2.EDTTryStopDeviceRequestNewResources
title: IWDTFPNPAction2::EDTTryStopDeviceRequestNewResources method
author: windows-driver-content
description: Attempts to send an IRP_MN_STOP_DEVICE event to the target device and assign new resources to the target device.
old-location: dtf\iwdtfpnpaction2_edttrystopdevicerequestnewresources.htm
old-project: dtf
ms.assetid: 19d3a72c-f7a5-483c-9fd1-5853c0a3e906
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IWDTFPNPAction2::EDTTryStopDeviceRequestNewResources, Microsoft.WDTF.IWDTFPNPAction2.EDTTryStopDeviceRequestNewResources, EDTTryStopDeviceRequestNewResources method [Windows Device Testing Framework], Microsoft::WDTF::IWDTFPNPAction2::EDTTryStopDeviceRequestNewResources, EDTTryStopDeviceRequestNewResources method [Windows Device Testing Framework], IWDTFPNPAction2 interface, EDTTryStopDeviceRequestNewResources, wdtfpnpaction/IWDTFPNPAction2::EDTTryStopDeviceRequestNewResources, dtf.iwdtfpnpaction2_edttrystopdevicerequestnewresources, IWDTFPNPAction2, IWDTFPNPAction2 interface [Windows Device Testing Framework], EDTTryStopDeviceRequestNewResources method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfpnpaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFPNPAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverPNPAction.Interop.dll
req.type-library: 
req.lib: wdtfpnpaction.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTFDriverPNPAction.Interop.dll
apiname:
-	IWDTFPNPAction2.EDTTryStopDeviceRequestNewResources
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFPNPAction2::EDTTryStopDeviceRequestNewResources method


## -description


Attempts to send an IRP_MN_STOP_DEVICE event to the target device and 
assign new resources to the target device.


## -syntax


````
HRESULT EDTTryStopDeviceRequestNewResources(
  [out, retval] VARIANT_BOOL *pbSuccess
);
````


## -parameters




### -param pbSuccess [out, retval]

True if the operation succeeds; otherwise, false.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/8fc225af-09d4-42a0-a862-4af89addd5f8">IWDTFEnhancedDeviceTestSupportAction2::Enable</a>  
method must be called for the target device before calling this method.</div>
<div> </div>
Similar to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451077">EDTTryStopDevice</a> method, 
<b>EDTTryStopDeviceRequestNewResources</b> attempts to trigger a PnP resource 
rebalance (e.g. IRP_MN_STOP_DEVICE) on the target device stack, with the addition that the method 
attempts to force the device onto a new set of hardware resources.

The Stop IRP is not guaranteed. Other drivers on the stack can fail the IRP_MN_QUERY_STOP_DEVICE event
which precedes the Stop IRP (resulting in IRP_MN_CANCEL_STOP_DEVICE). Also, the system may 
optimize if it detects that the target device does not use hardware resources (e.g. a USB mouse) 
and send a CancelStop IRP instead.

If your device does not consume hardware resources but you still wish to attempt to test 
how the drivers and applications handle the PnP resource rebalance, you can instead run 
<b>EDTTryStopDeviceRequestNewResources</b> on a parent device, grandparent, 
etc., which does consume hardware resources. For example, if your device is a USB mouse, you can 
run this method on the parent USB controller instead.




## -see-also

<a href="..\wdtfpnpaction\nn-wdtfpnpaction-iwdtfpnpaction2.md">IWDTFPNPAction2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFPNPAction2::EDTTryStopDeviceRequestNewResources method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

