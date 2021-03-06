---
UID: NE:wdfdriver._WDF_DRIVER_INIT_FLAGS
title: "_WDF_DRIVER_INIT_FLAGS"
author: windows-driver-content
description: The WDF_DRIVER_INIT_FLAGS enumeration specifies driver initialization flags.
old-location: wdf\wdf_driver_init_flags.htm
old-project: wdf
ms.assetid: cbabd178-3496-4851-9acf-f0718eaebdcd
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdfdriver/WDF_DRIVER_INIT_FLAGS, WDF_DRIVER_INIT_FLAGS, DFDriverObjectRef_a77b530c-fd37-4ffe-a006-7deaa8156040.xml, wdfdriver/WdfDriverInitNonPnpDriver, wdfdriver/WdfVerifierOn, WdfVerifierOn, wdf.wdf_driver_init_flags, WdfDriverInitNoDispatchOverride, kmdf.wdf_driver_init_flags, _WDF_DRIVER_INIT_FLAGS, WdfVerifyOn, wdfdriver/WdfDriverInitNoDispatchOverride, WDF_DRIVER_INIT_FLAGS enumeration, WdfDriverInitNonPnpDriver, wdfdriver/WdfVerifyOn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdfdriver.h
req.include-header: Wdf.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
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
-	wdfdriver.h
apiname:
-	WDF_DRIVER_INIT_FLAGS
product: Windows
targetos: Windows
req.typenames: WDF_DRIVER_INIT_FLAGS
req.product: Windows 10 or later.
---

# _WDF_DRIVER_INIT_FLAGS enumeration


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The WDF_DRIVER_INIT_FLAGS enumeration specifies driver initialization flags.


## -syntax


````
typedef enum _WDF_DRIVER_INIT_FLAGS { 
  WdfDriverInitNonPnpDriver        = 0x00000001,
  WdfDriverInitNoDispatchOverride  = 0x00000002,
  WdfVerifyOn                      = 0x00000004,
  WdfVerifierOn                    = 0x00000008
} WDF_DRIVER_INIT_FLAGS;
````


## -enum-fields




### -field WdfDriverInitNonPnpDriver

The driver does not support Plug and Play (PnP). If this value is set, the driver must not supply an <a href="..\wdfdriver\nc-wdfdriver-evt_wdf_driver_device_add.md">EvtDriverDeviceAdd</a> callback function. For more information about non-PnP drivers, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-kernel-mode-driver-framework-with-non-pnp-drivers">Using Kernel-Mode Driver Framework with Non-PnP Drivers</a>.


### -field WdfDriverInitNoDispatchOverride

The driver is a miniport driver and, therefore, the framework must not provide dispatch routines for the driver. In other words, the framework must not intercept I/O request packets (IRPs) that the I/O manager has directed to the driver. In addition, the driver must call <a href="..\wdfminiport\nf-wdfminiport-wdfdriverminiportunload.md">WdfDriverMiniportUnload</a> when the port driver informs the miniport driver that it is about to be unloaded. For more information about this flag and how to write framework-based miniport drivers, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/creating-kmdf-miniport-drivers">Using Kernel-Mode Driver Framework with Miniport Drivers</a>.


### -field WdfVerifyOn

Reserved for system use. Drivers must not use this flag.


### -field WdfVerifierOn

Reserved for system use. Drivers must not use this flag.


### -field WdfDriverInitCompanion




## -remarks



The WDF_DRIVER_INIT_FLAGS enumeration is used to specify the value for the <b>DriverInitFlags</b> member of the <a href="..\wdfdriver\ns-wdfdriver-_wdf_driver_config.md">WDF_DRIVER_CONFIG</a> structure.




## -see-also

<a href="..\wdfdriver\ns-wdfdriver-_wdf_driver_config.md">WDF_DRIVER_CONFIG</a>



<a href="..\wdfminiport\nf-wdfminiport-wdfdriverminiportunload.md">WdfDriverMiniportUnload</a>



<a href="..\wdfdriver\nc-wdfdriver-evt_wdf_driver_device_add.md">EvtDriverDeviceAdd</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_DRIVER_INIT_FLAGS enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

