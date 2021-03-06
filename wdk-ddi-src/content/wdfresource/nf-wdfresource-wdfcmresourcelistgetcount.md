---
UID: NF:wdfresource.WdfCmResourceListGetCount
title: WdfCmResourceListGetCount function
author: windows-driver-content
description: The WdfCmResourceListGetCount method returns the number of resource descriptors that are contained in a specified resource list.
old-location: wdf\wdfcmresourcelistgetcount.htm
old-project: wdf
ms.assetid: f1a38276-4964-422d-9b3c-8450b1028f27
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.wdfcmresourcelistgetcount, DFResourceObjectRef_8161cc12-7f39-44f4-a4a1-28329911ac96.xml, WdfCmResourceListGetCount method, wdfresource/WdfCmResourceListGetCount, WdfCmResourceListGetCount, kmdf.wdfcmresourcelistgetcount, PFN_WDFCMRESOURCELISTGETCOUNT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfresource.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (KMDF); WUDFx02000.dll (UMDF)
req.dll: 
req.irql: "<=DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	LibDef
apilocation:
-	Wdf01000.sys
-	Wdf01000.sys.dll
-	WUDFx02000.dll
-	WUDFx02000.dll.dll
apiname:
-	WdfCmResourceListGetCount
product: Windows
targetos: Windows
req.typenames: "*PWDF_REQUEST_SEND_OPTIONS, WDF_REQUEST_SEND_OPTIONS"
req.product: Windows 10 or later.
---

# WdfCmResourceListGetCount function


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WdfCmResourceListGetCount</b> method returns the number of resource descriptors that are contained in a specified resource list.


## -syntax


````
ULONG WdfCmResourceListGetCount(
  _In_ WDFCMRESLIST List
);
````


## -parameters




### -param List [in]

A handle to a framework resource-list object that represents a list of hardware resources for a device.


## -returns



<b>WdfCmResourceListGetCount</b> returns the number of resource descriptors that are contained in the resource list that the <i>List</i> parameter specifies.

A system bug check occurs if the driver supplies an invalid object handle.






## -remarks



For more information about resource lists, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/hardware-resources-for-kmdf-drivers">Hardware Resources for Framework-Based Drivers</a>.


#### Examples

The following code example shows how an <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_prepare_hardware.md">EvtDevicePrepareHardware</a> callback function might locate the memory, port, and interrupt resources in the list of <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/raw-and-translated-resources">translated hardware resources</a> that the Plug and Play (PnP) manager has assigned to a device.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>NTSTATUS
MyEvtDevicePrepareHardware (
    WDFDEVICE  Device,
    WDFCMRESLIST  Resources,
    WDFCMRESLIST  ResourcesTranslated
    )
{
    ULONG  i;
    PCM_PARTIAL_RESOURCE_DESCRIPTOR  desc;

    for (i = 0; i &lt; WdfCmResourceListGetCount(ResourcesTranslated); i++) {

        desc = WdfCmResourceListGetDescriptor(
                                              ResourcesTranslated,
                                              i
                                              );

        switch (desc-&gt;Type) {

            case CmResourceTypeMemory:
                //
                // Handle memory resources here.
                //
                break;

            case CmResourceTypePort:
                //
                // Handle port resources here.
                //
                break;

            case CmResourceTypeInterrupt:
                //
                // Handle interrupt resources here.
                //
                break;
            default:
                //
                // Ignore all other descriptors.
                //
                break;
        }
    }
}</pre>
</td>
</tr>
</table></span></div>


