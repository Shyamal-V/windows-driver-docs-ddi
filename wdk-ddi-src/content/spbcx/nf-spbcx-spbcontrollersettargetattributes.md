---
UID: NF:spbcx.SpbControllerSetTargetAttributes
title: SpbControllerSetTargetAttributes function
author: windows-driver-content
description: The SpbControllerSetTargetAttributes method sets object attributes that will be used for all SPBTARGET objects that the SPB framework extension (SpbCx) delivers to the SPB controller driver.
old-location: spb\spbcontrollersettargetattributes.htm
old-project: SPB
ms.assetid: 8EC415AA-F578-42BF-B785-52613B20A2AC
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: spbcx/SpbControllerSetTargetAttributes, SPB.spbcontrollersettargetattributes, SpbControllerSetTargetAttributes, SpbControllerSetTargetAttributes method [Buses]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: spbcx.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 8.
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
req.lib: Spbcxstubs.lib
req.dll: 
req.irql: PASSIVE_LEVEL
topictype:
-	APIRef
-	kbSyntax
apitype:
-	LibDef
apilocation:
-	spbcxstubs.lib
-	spbcxstubs.dll
apiname:
-	SpbControllerSetTargetAttributes
product: Windows
targetos: Windows
req.typenames: "*PSPB_REQUEST_TYPE, SPB_REQUEST_TYPE"
req.product: Windows 10 or later.
---

# SpbControllerSetTargetAttributes function


## -description


The <b>SpbControllerSetTargetAttributes</b> method sets object attributes that will be used for all SPBTARGET objects that the SPB framework extension (SpbCx) delivers to the SPB controller driver.


## -syntax


````
VOID SpbControllerSetTargetAttributes(
  _In_ WDFDEVICE              FxDevice,
  _In_ PWDF_OBJECT_ATTRIBUTES ObjectAttributes
);
````


## -parameters




### -param FxDevice [in]

A WDFDEVICE handle to the device object that represents the SPB controller.


### -param ObjectAttributes [in]

A pointer to a caller-allocated <a href="..\wdfobject\ns-wdfobject-_wdf_object_attributes.md">WDF_OBJECT_ATTRIBUTES</a> structure that contains attributes for the controller's SPBTARGET objects.


## -returns



None.




## -remarks



Your SPB controller driver calls this method to set the default attributes for SPBTARGET objects.  The SPB framework extension (SpbCx) sets these attributes on any target devices on the bus that are opened by clients (peripheral devices) of the controller.

<i>ObjectAttributes</i> points to an <b>WDF_OBJECT_ATTRIBUTES</b> structure. The caller must previously have called the <a href="..\wdfobject\nf-wdfobject-wdf_object_attributes_init.md">WDF_OBJECT_ATTRIBUTES_INIT</a> function to initialize this structure. After this call, but before the call to <b>SpbControllerSetTargetAttributes</b>, the caller can change the values of the following members of this structure:

<ul>
<li><b>EvtCleanupCallback</b></li>
<li><b>EvtDestroyCallback</b></li>
<li><b>ContextSizeOverride</b></li>
<li><b>ContextTypeInfo</b></li>
</ul>
<b>SpbControllerSetTargetAttributes</b> will use these values as default attributes for SPBTARGET objects. However, the driver cannot change the default attribute values that are contained in the <b>ExecutionLevel</b>, <b>SynchronizationScope</b>, and <b>ParentObject</b> members.  These members must remain unchanged from the values that they were initialized to by the <b>WDF_OBJECT_ATTRIBUTES_INIT</b> function.

The SPB controller driver must call this method before it <i>commits</i> the device object—that is, before it returns from the <a href="..\wdfdriver\nc-wdfdriver-evt_wdf_driver_device_add.md">EvtDriverDeviceAdd</a> callback or adds the PDO to the controller's child list. The child list represents the devices that are attached to the bus. For more information, see <a href="https://msdn.microsoft.com/5731db82-2bc8-4a8d-98f1-3977845f572c">Enumerating the Devices on a Bus</a>.




## -see-also

<a href="..\wdfobject\ns-wdfobject-_wdf_object_attributes.md">WDF_OBJECT_ATTRIBUTES</a>



<a href="..\wdfobject\nf-wdfobject-wdf_object_attributes_init.md">WDF_OBJECT_ATTRIBUTES_INIT</a>



<a href="..\wdfdriver\nc-wdfdriver-evt_wdf_driver_device_add.md">EvtDriverDeviceAdd</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [SPB\buses]:%20SpbControllerSetTargetAttributes method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

