---
UID: NE:portcls.PC_REBALANCE_TYPE
title: PC_REBALANCE_TYPE
author: windows-driver-content
description: The PC_REBALANCE_TYPE enum describes the type of support for rebalancing.
old-location: audio\pc_rebalance_type.htm
old-project: audio
ms.assetid: CE700126-8C29-4218-9248-F722523A4DA3
ms.author: windowsdriverdev
ms.date: 2/8/2018
ms.keywords: audio.pc_rebalance_type, portcls/PC_REBALANCE_TYPE, PC_REBALANCE_TYPE, PcRebalanceNotSupported, portcls/PcRebalanceNotSupported, PcRebalanceRemoveSubdevices, portcls/PcRebalanceRemoveSubdevices, PC_REBALANCE_TYPE enumeration [Audio Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: portcls.h
req.include-header: Portcls.h
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
-	portcls.h
apiname:
-	PC_REBALANCE_TYPE
product: Windows
targetos: Windows
req.typenames: PC_REBALANCE_TYPE
---

# PC_REBALANCE_TYPE enumeration


## -description


The <code>PC_REBALANCE_TYPE</code> enum describes the type of support for rebalancing.


## -syntax


````
typedef enum _PC_REBALANCE_TYPE { 
  PcRebalanceNotSupported      = 0,
  PcRebalanceRemoveSubdevices  = 
} PC_REBALANCE_TYPE;
````


## -enum-fields




### -field PcRebalanceNotSupported

Indicates that PcRebalance is not supported. 


### -field PcRebalanceRemoveSubdevices

Indicates that PcRebalance is supported via unregistering and re-registering the audio subdevices.


## -remarks



 Rebalancing is used in certain PCI scenarios. For example when additional devices are added to the PCI chain and the use of memory resources needs to be rearranged and consolidated.

For more information,  see <a href="https://msdn.microsoft.com/FCAD7F8B-AA9B-430A-BCAF-04E13FA15382">Implement PnP Rebalance for PortCls Audio Drivers</a>.

Available in Windows 10, version 1511 and later versions of Windows. 



