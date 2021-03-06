---
UID: NS:ntddtape._TAPE_CREATE_PARTITION
title: "_TAPE_CREATE_PARTITION"
author: windows-driver-content
description: The TAPE_CREATE_PARTITION structure is used in conjunction with the IOCTL_TAPE_CREATE_PARTITION request to create a specified number of fixed, select, or initiator partitions of a given size on the tape media.
old-location: storage\tape_create_partition.htm
old-project: storage
ms.assetid: 5020d2c6-f435-4d22-98a3-23318ffc0baf
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: ntddtape/PTAPE_CREATE_PARTITION, TAPE_CREATE_PARTITION structure [Storage Devices], *PTAPE_CREATE_PARTITION, TAPE_CREATE_PARTITION, ntddtape/TAPE_CREATE_PARTITION, structs-tape_3d86a9f7-45b2-48e8-ae21-2ad87641bcf9.xml, PTAPE_CREATE_PARTITION structure pointer [Storage Devices], storage.tape_create_partition, PTAPE_CREATE_PARTITION, _TAPE_CREATE_PARTITION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddtape.h
req.include-header: Ntddtape.h
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
-	ntddtape.h
apiname:
-	TAPE_CREATE_PARTITION
product: Windows
targetos: Windows
req.typenames: "*PTAPE_CREATE_PARTITION, TAPE_CREATE_PARTITION"
---

# _TAPE_CREATE_PARTITION structure


## -description


The TAPE_CREATE_PARTITION structure is used in conjunction with the <a href="..\ntddtape\ni-ntddtape-ioctl_tape_create_partition.md">IOCTL_TAPE_CREATE_PARTITION</a> request to create a specified number of fixed, select, or initiator partitions of a given size on the tape media.


## -syntax


````
typedef struct _TAPE_CREATE_PARTITION {
  ULONG Method;
  ULONG Count;
  ULONG Size;
} TAPE_CREATE_PARTITION, *PTAPE_CREATE_PARTITION;
````


## -struct-fields




### -field Method

Indicates the method used to create the partitions. This member can have one of the following values: 

<table>
<tr>
<th>Method</th>
<th>Meaning</th>
</tr>
<tr>
<td>
TAPE_FIXED_PARTITIONS

</td>
<td>
Partitions the tape based on the device's default definition of partitions. The <b>Count</b> and <b>Size</b> parameters are ignored. 

</td>
</tr>
<tr>
<td>
TAPE_SELECT_PARTITIONS

</td>
<td>
Partitions the tape into the number of partitions specified by <b>Count</b>. The <b>Size</b> parameter is ignored. The size of the partitions is determined by the device's default partition size. For more specific information, refer to the documentation for your tape device.

</td>
</tr>
<tr>
<td>
TAPE_INITIATOR_PARTITIONS

</td>
<td>
Partitions the tape into the number and size of partitions specified by <b>Count</b> and <b>Size</b>, respectively, except for the last partition. The size of the last partition is the remainder of the tape. 

</td>
</tr>
</table>
 


### -field Count

Indicates the number of partitions to create.


### -field Size

Indicates the size of each partition, in bytes.


## -see-also

<a href="..\minitape\nc-minitape-tape_process_command_routine.md">TapeMiniCreatePartition</a>



<a href="..\ntddtape\ni-ntddtape-ioctl_tape_create_partition.md">IOCTL_TAPE_CREATE_PARTITION</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20TAPE_CREATE_PARTITION structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

