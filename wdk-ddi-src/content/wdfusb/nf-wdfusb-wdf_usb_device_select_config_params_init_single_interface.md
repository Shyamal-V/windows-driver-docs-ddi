---
UID: NF:wdfusb.WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE
title: WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE function
author: windows-driver-content
description: The WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE function initializes a WDF_USB_DEVICE_SELECT_CONFIG_PARAMS structure so that a driver can configure a device to use a single, specified interface.
old-location: wdf\wdf_usb_device_select_config_params_init_single_interface.htm
old-project: wdf
ms.assetid: c0dfcc32-7a32-4d76-b954-de2c9c188353
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdfusb/WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE, DFUsbRef_a1c68810-efa7-4438-ab8b-ea6ea881d941.xml, wdf.wdf_usb_device_select_config_params_init_single_interface, WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE function, kmdf.wdf_usb_device_select_config_params_init_single_interface, WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfusb.h
req.include-header: Wdfusb.h
req.target-type: Universal
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	wdfusb.h
apiname:
-	WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE
product: Windows
targetos: Windows
req.typenames: "*PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE"
req.product: Windows 10 or later.
---

# WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE function


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE</b> function initializes a <a href="..\wdfusb\ns-wdfusb-_wdf_usb_device_select_config_params.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</a> structure so that a driver can configure a device to use a single, specified interface. 


## -syntax


````
VOID WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE(
  _Out_ PWDF_USB_DEVICE_SELECT_CONFIG_PARAMS Params
);
````


## -parameters




### -param Params [out]

A pointer to a driver-allocated <a href="..\wdfusb\ns-wdfusb-_wdf_usb_device_select_config_params.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</a> structure.


## -returns



None




## -remarks



Your driver can use the <b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE</b> function to select a configuration if the device interface is specified by a handle to USB interface objects. 

Your driver can use this function only if your device has just one USB interface.

The <b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE</b> function zeros the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_device_select_config_params.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</a> structure and sets the <b>Size</b> member to the size of the structure. It also sets the <b>Type</b> member to <b>WdfUsbTargetDeviceSelectConfigTypeSingleInterface</b>.

To initialize a <a href="..\wdfusb\ns-wdfusb-_wdf_usb_device_select_config_params.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</a> structure, the driver must call one of the following functions:

<ul>
<li>

<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_deconfig.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_DECONFIG</a>


</li>
<li>
<b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE</b>

</li>
<li>

<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_multiple_interfaces.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_MULTIPLE_INTERFACES</a>


</li>
<li>

<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_interfaces_descriptors.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_INTERFACES_DESCRIPTORS</a>


</li>
<li>

<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_urb.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_URB</a>


</li>
</ul>
For a code example that uses <b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE</b>, see <a href="..\wdfusb\nf-wdfusb-wdfusbtargetdeviceselectconfig.md">WdfUsbTargetDeviceSelectConfig</a>.




## -see-also

<a href="..\wdfusb\ns-wdfusb-_wdf_usb_device_select_config_params.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_single_interface.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_urb.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_URB</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_deconfig.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_DECONFIG</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_multiple_interfaces.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_MULTIPLE_INTERFACES</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_interfaces_descriptors.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_INTERFACES_DESCRIPTORS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

