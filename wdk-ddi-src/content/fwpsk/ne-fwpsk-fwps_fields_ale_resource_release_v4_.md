---
UID: NE:fwpsk.FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4_
title: FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4_
author: windows-driver-content
description: The FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4 enumeration type specifies the data field identifiers for the FWPS_LAYER_ALE_RESOURCE_RELEASE_V4 run-time filtering layer.
old-location: netvista\fwps_fields_ale_resource_release_v4.htm
old-project: netvista
ms.assetid: ad3d3099-58eb-4a34-b15c-a323dcedba84
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS_TYPE, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_PORT, FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_MAX, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_PACKAGE_ID, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_PORT, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_INTERFACE, wfp_ref_5_const_3_data_fields_09378323-ec5f-4db4-89d3-8398e4b76fac.xml, fwpsk/FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4, netvista.fwps_fields_ale_resource_release_v4, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_USER_ID, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_PACKAGE_ID, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS_TYPE, FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4 enumeration [Network Drivers Starting with Windows Vista], fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_APP_ID, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_FLAGS, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_INTERFACE, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_FLAGS, FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4_, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_USER_ID, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_MAX, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_APP_ID, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_PROTOCOL, fwpsk/FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS, FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_PROTOCOL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fwpsk.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 7.
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
req.irql: "<= DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	fwpsk.h
apiname:
-	FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4
product: Windows
targetos: Windows
req.typenames: FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4
---

# FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4_ enumeration


## -description


The FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4 enumeration type specifies the data field identifiers for the
  FWPS_LAYER_ALE_RESOURCE_RELEASE_V4 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layer</a>.


## -syntax


````
typedef enum FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4_ { 
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_APP_ID,
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_USER_ID,
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS,
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS_TYPE,
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_PORT,
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_PROTOCOL,
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_INTERFACE,
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_FLAGS,
#if (NTDDI_VERSION >= NTDDI_WIN8)
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_PACKAGE_ID,
#endif 
  FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_MAX
} FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4;
````


## -enum-fields




### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_APP_ID

The full path of the application.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_USER_ID

The identifier of the local user.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS

The local IP address.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_ADDRESS_TYPE

The local IP address type. The possible values are defined by the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a> enumeration.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_PORT

The local transport protocol port number.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_PROTOCOL

The IP protocol number, as specified in RFC 1700.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_IP_LOCAL_INTERFACE

The locally unique identifier (<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>) for the network interface associated with the
     local IP address.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible
     flags, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff549942">Filtering Condition Flags</a>.


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_PACKAGE_ID

The package identifier is a security identifier (SID) that identifies the associated AppContainer process. For more information about the SID structure, see the description for the SID structure in the Microsoft Windows SDK documentation.

<div class="alert"><b>Note</b>  Supported starting with Windows 8.</div>
<div> </div>

### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_ALE_SECURITY_ATTRIBUTE_FQBN_VALUE


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_COMPARTMENT_ID


### -field FWPS_FIELD_ALE_RESOURCE_RELEASE_V4_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.


## -see-also

<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_FIELDS_ALE_RESOURCE_RELEASE_V4 enumeration%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

