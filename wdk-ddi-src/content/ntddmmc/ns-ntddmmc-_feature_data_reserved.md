---
UID: NS:ntddmmc._FEATURE_DATA_RESERVED
title: "_FEATURE_DATA_RESERVED"
author: windows-driver-content
description: The FEATURE_DATA_RESERVED structure holds information about an unspecified feature.
old-location: storage\feature_data_reserved.htm
old-project: storage
ms.assetid: 686bc6e0-7455-4b86-93ce-09b7c7d60240
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: FEATURE_DATA_RESERVED structure [Storage Devices], storage.feature_data_reserved, PFEATURE_DATA_RESERVED structure pointer [Storage Devices], _FEATURE_DATA_RESERVED, structs-CD-ROM_4fc9f24f-2488-493d-8e63-2e4c8a3ab879.xml, FEATURE_DATA_RESERVED, PFEATURE_DATA_RESERVED, *PFEATURE_DATA_RESERVED, ntddmmc/PFEATURE_DATA_RESERVED, ntddmmc/FEATURE_DATA_RESERVED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddmmc.h
req.include-header: Ntddcdrm.h
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
req.irql: PASSIVE_LEVEL
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	ntddmmc.h
apiname:
-	FEATURE_DATA_RESERVED
product: Windows
targetos: Windows
req.typenames: "*PFEATURE_DATA_RESERVED, FEATURE_DATA_RESERVED"
---

# _FEATURE_DATA_RESERVED structure


## -description


The FEATURE_DATA_RESERVED structure holds information about an unspecified feature. 


## -syntax


````
typedef struct _FEATURE_DATA_RESERVED {
  FEATURE_HEADER Header;
  UCHAR          Data[];
} FEATURE_DATA_RESERVED, *PFEATURE_DATA_RESERVED;
````


## -struct-fields




### -field Header

Contains a <a href="..\ntddmmc\ns-ntddmmc-_feature_header.md">FEATURE_HEADER</a> structure with header information for this feature descriptor. 


### -field Data

Contains an array describing unspecified feature structure members. 


## -remarks



You can use this structure to access the data of any feature structure as though it were a simple character array.  




## -see-also

<a href="..\ntddmmc\ns-ntddmmc-_feature_header.md">FEATURE_HEADER</a>



<a href="..\ntddmmc\ne-ntddmmc-_feature_number.md">FEATURE_NUMBER</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20FEATURE_DATA_RESERVED structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

