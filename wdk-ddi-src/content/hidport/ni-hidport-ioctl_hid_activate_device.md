---
UID: NI:hidport.IOCTL_HID_ACTIVATE_DEVICE
title: IOCTL_HID_ACTIVATE_DEVICE
author: windows-driver-content
description: The IOCTL_HID_ACTIVATE_DEVICE request activates a HIDClass device, which makes it ready for I/O operations.
old-location: hid\ioctl_hid_activate_device.htm
old-project: hid
ms.assetid: 5d2f218c-a9a5-4149-8fde-898171dfc9a7
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: hid.ioctl_hid_activate_device, IOCTL_HID_ACTIVATE_DEVICE control code [Human Input Devices], IOCTL_HID_ACTIVATE_DEVICE, hidport/IOCTL_HID_ACTIVATE_DEVICE, hidioreq_031bb843-02fe-4859-acf2-4bcbfaaea657.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: hidport.h
req.include-header: Hidport.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	hidport.h
apiname:
-	IOCTL_HID_ACTIVATE_DEVICE
product: Windows
targetos: Windows
req.typenames: "*PUSAGE_AND_PAGE, USAGE_AND_PAGE"
---

# IOCTL_HID_ACTIVATE_DEVICE IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


The IOCTL_HID_ACTIVATE_DEVICE request activates a HIDClass device, which makes it ready for I/O operations.

For general information about HIDClass devices, see <a href="https://msdn.microsoft.com/2d3efb38-4eba-43db-8cff-9fac30209952">HID Collections</a>. 


## -ioctlparameters




### -input-buffer

<b>Parameters.DeviceIoControl.Type3InputBuffer</b> contains a collection identifier, as a ULONG value, of the collection to activate.


### -input-buffer-length

The length of a ULONG value.


### -output-buffer

None.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block


       HID minidrivers that carry out the I/O to the device set the following fields of <b>Irp-&gt;IoStatus</b>:

<ul>
<li>
<b>Information</b> is set to zero.

</li>
<li>
<b>Status</b> is set to STATUS_SUCCESS if the transfer completed without error. Otherwise, it is set to an appropriate NTSTATUS error code.

</li>
</ul>
Minidrivers that call other drivers with this IRP to carry out the I/O to their device should ensure that the <b>Information</b> field of the status block is zero and not change the contents of the <b>Status</b> field.


## -see-also

<a href="..\hidport\ni-hidport-ioctl_hid_deactivate_device.md">IOCTL_HID_DEACTIVATE_DEVICE</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [hid\hid]:%20IOCTL_HID_ACTIVATE_DEVICE control code%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

