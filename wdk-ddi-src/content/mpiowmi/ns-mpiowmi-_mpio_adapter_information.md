---
UID: NS:mpiowmi._MPIO_ADAPTER_INFORMATION
title: "_MPIO_ADAPTER_INFORMATION"
author: windows-driver-content
description: The MPIO_ADAPTER_INFORMATION structure contains information that pertains to MPIO's view of a path.
old-location: storage\mpio_adapter_information.htm
old-project: storage
ms.assetid: bcf159a7-75a5-46aa-897a-2c5eb00f51d8
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: mpiowmi/PMPIO_ADAPTER_INFORMATION, storage.mpio_adapter_information, structs-scsibus_bcdbb143-5a91-4a69-83e5-82e32c23b404.xml, mpiowmi/MPIO_ADAPTER_INFORMATION, MPIO_ADAPTER_INFORMATION structure [Storage Devices], MPIO_ADAPTER_INFORMATION, _MPIO_ADAPTER_INFORMATION, *PMPIO_ADAPTER_INFORMATION, PMPIO_ADAPTER_INFORMATION, PMPIO_ADAPTER_INFORMATION structure pointer [Storage Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mpiowmi.h
req.include-header: Mpiowmi.h
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
-	mpiowmi.h
apiname:
-	MPIO_ADAPTER_INFORMATION
product: Windows
targetos: Windows
req.typenames: "*PMPIO_ADAPTER_INFORMATION, MPIO_ADAPTER_INFORMATION"
---

# _MPIO_ADAPTER_INFORMATION structure


## -description


The MPIO_ADAPTER_INFORMATION structure contains information that pertains to MPIO's view of a path.


## -syntax


````
typedef struct _MPIO_ADAPTER_INFORMATION {
  ULONGLONG PathId;
  UCHAR     BusNumber;
  UCHAR     DeviceNumber;
  UCHAR     FunctionNumber;
  UCHAR     Pad;
  WCHAR     AdapterName[63 + 1];
} MPIO_ADAPTER_INFORMATION, *PMPIO_ADAPTER_INFORMATION;
````


## -struct-fields




### -field PathId

An unsigned 64-bitfield that represents an identifier that is assigned to a particular path. This field will match the PathIdentifier field in the instance(s) of the PDO_INFORMATION class that represent device(s) exposed via this path.


### -field BusNumber

An unsigned 8-bitfield that corresponds to the bus number that is assigned by PCI to the host bus adapter through which this path is exposed.


### -field DeviceNumber

An unsigned 8-bitfield that corresponds to the device number that is assigned by PCI to the host bus adapter through which this path is exposed.


### -field FunctionNumber

An unsigned 8-bitfield that corresponds to the function number that is assigned by PCI to the host bus adapter through which this path is exposed.


### -field Pad

Should be zero.


### -field AdapterName

A string field that returns the friendly name of the host bus adapter through which this path is exposed.

