---
UID: NF:wdfchildlist.WdfChildListRetrieveAddressDescription
title: WdfChildListRetrieveAddressDescription function
author: windows-driver-content
description: The WdfChildListRetrieveAddressDescription method locates a child device that has a specified identification description and retrieves the device's address description.
old-location: wdf\wdfchildlistretrieveaddressdescription.htm
old-project: wdf
ms.assetid: 0c551de0-970a-4733-b904-27c40cf7b42f
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.wdfchildlistretrieveaddressdescription, WdfChildListRetrieveAddressDescription method, kmdf.wdfchildlistretrieveaddressdescription, PFN_WDFCHILDLISTRETRIEVEADDRESSDESCRIPTION, WdfChildListRetrieveAddressDescription, wdfchildlist/WdfChildListRetrieveAddressDescription, DFDeviceObjectChildListRef_bd30cd1e-b7ac-40cd-b96f-4071d08bafc1.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfchildlist.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 
req.ddi-compliance: DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (see Framework Library Versioning.)
req.dll: 
req.irql: "<= DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	LibDef
apilocation:
-	Wdf01000.sys
-	Wdf01000.sys.dll
apiname:
-	WdfChildListRetrieveAddressDescription
product: Windows
targetos: Windows
req.typenames: WDF_RETRIEVE_CHILD_FLAGS
req.product: Windows 10 or later.
---

# WdfChildListRetrieveAddressDescription function


## -description


<p class="CCE_Message">[Applies to KMDF only]

The <b>WdfChildListRetrieveAddressDescription</b> method locates a child device that has a specified <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/dynamic-enumeration">identification description</a> and retrieves the device's <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/dynamic-enumeration">address description</a>.


## -syntax


````
NTSTATUS WdfChildListRetrieveAddressDescription(
  _In_    WDFCHILDLIST                                 ChildList,
  _In_    PWDF_CHILD_IDENTIFICATION_DESCRIPTION_HEADER IdentificationDescription,
  _Inout_ PWDF_CHILD_ADDRESS_DESCRIPTION_HEADER        AddressDescription
);
````


## -parameters




### -param ChildList [in]

A handle to a child list object.


### -param IdentificationDescription [in]

A pointer to a caller-allocated <a href="..\wdfchildlist\ns-wdfchildlist-_wdf_child_identification_description_header.md">WDF_CHILD_IDENTIFICATION_DESCRIPTION_HEADER</a> structure that identifies a driver-supplied child identification description.


### -param AddressDescription [in, out]

A pointer to a <a href="..\wdfchildlist\ns-wdfchildlist-_wdf_child_address_description_header.md">WDF_CHILD_ADDRESS_DESCRIPTION_HEADER</a> structure that identifies a child address description. The framework fills in this description.


## -returns



<b>WdfChildListRetrieveAddressDescription</b> returns STATUS_SUCCESS, or another status value for which <a href="https://msdn.microsoft.com/fe823930-e3ff-4c95-a640-bb6470c95d1d">NT_SUCCESS(status)</a> equals <b>TRUE</b>, if the operation succeeds. Otherwise, this method might return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An input parameter was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
No device matched the specified identification description.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DEVICE_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The child list did not contain address descriptions, or the size of the address description that <i>AddressDescription</i> specified was incorrect.

</td>
</tr>
</table>
 

This method might also return other <a href="https://msdn.microsoft.com/library/windows/hardware/ff557697">NTSTATUS values</a>.



A system bug check occurs if the driver supplies an invalid object handle.





## -remarks



For more information about child lists, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/dynamic-enumeration">Dynamic Enumeration</a>.


#### Examples

The following code example searches a child list for a child device whose identification description contains the value that is specified by <b>SomeValue</b>. If <b>WdfChildListRetrieveAddressDescription</b> locates the device, it retrieves the device's address description.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>MY_IDENTIFICATION_DESCRIPTION  id;
MY_ADDRESS_DESCRIPTION  addrDescrip;

WDF_CHILD_IDENTIFICATION_DESCRIPTION_HEADER_INIT(
                                                 &amp;id.Header,
                                                 sizeof(id)
                                                 );
WDF_CHILD_ADDRESS_DESCRIPTION_HEADER_INIT(
                                          &amp;addrDescrip.Header,
                                          sizeof(addrDescrip)
                                          );

id.DeviceIdentifier = SomeValue;
status = WdfChildListRetrieveAddressDescription(
                                                list,
                                                &amp;idDescrip.Header,
                                                &amp;addrDescrip.Header
                                                );
if (!NT_SUCCESS(status) {
    return status;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also

<a href="..\wdfchildlist\nf-wdfchildlist-wdf_child_identification_description_header_init.md">WDF_CHILD_IDENTIFICATION_DESCRIPTION_HEADER_INIT</a>



<a href="..\wdfchildlist\ns-wdfchildlist-_wdf_child_identification_description_header.md">WDF_CHILD_IDENTIFICATION_DESCRIPTION_HEADER</a>



<a href="..\wdfchildlist\ns-wdfchildlist-_wdf_child_address_description_header.md">WDF_CHILD_ADDRESS_DESCRIPTION_HEADER</a>



<a href="..\wdfchildlist\nf-wdfchildlist-wdf_child_address_description_header_init.md">WDF_CHILD_ADDRESS_DESCRIPTION_HEADER_INIT</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WdfChildListRetrieveAddressDescription method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

