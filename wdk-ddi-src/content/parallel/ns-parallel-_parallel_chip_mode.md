---
UID: NS:parallel._PARALLEL_CHIP_MODE
title: "_PARALLEL_CHIP_MODE"
author: windows-driver-content
description: The PARALLEL_CHIP_MODE structure specifies the operating mode of a parallel port.
old-location: parports\parallel_chip_mode.htm
old-project: parports
ms.assetid: e9d78c80-e6cf-49af-89de-6df8ea871796
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: PARALLEL_CHIP_MODE structure [Parallel Ports], *PPARALLEL_CHIP_MODE, PARALLEL_CHIP_MODE, cisspd_1dbc3693-e551-46a3-9a41-725b06a2ee9a.xml, _PARALLEL_CHIP_MODE, parports.parallel_chip_mode, parallel/PARALLEL_CHIP_MODE, PPARALLEL_CHIP_MODE structure pointer [Parallel Ports], parallel/PPARALLEL_CHIP_MODE, PPARALLEL_CHIP_MODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: parallel.h
req.include-header: Parallel.h
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
-	parallel.h
apiname:
-	PARALLEL_CHIP_MODE
product: Windows
targetos: Windows
req.typenames: PARALLEL_CHIP_MODE, *PPARALLEL_CHIP_MODE
---

# _PARALLEL_CHIP_MODE structure


## -description


The PARALLEL_CHIP_MODE structure specifies the operating mode of a parallel port.


## -syntax


````
typedef struct _PARALLEL_CHIP_MODE {
  UCHAR   ModeFlags;
  BOOLEAN success;
} PARALLEL_CHIP_MODE, *PPARALLEL_CHIP_MODE;
````


## -struct-fields




### -field ModeFlags

Specifies an operating mode of a parallel port, either an enhanced parallel port (EPP) mode or an extended capabilities port (ECP) mode.


### -field success

Not used.


## -remarks



A client uses a PARALLEL_CHIP_MODE structure with internal device control requests to set and clear the operating mode of a parallel port.

<div class="alert"><b>Note</b>    Microsoft does not recommend using a client-supplied interrupt routine. The use of interrupts might cause system instability. By default, the <a href="..\parallel\ni-parallel-ioctl_internal_parallel_connect_interrupt.md">IOCTL_INTERNAL_PARALLEL_CONNECT_INTERRUPT</a> request is disabled. For more information, see <a href="https://msdn.microsoft.com/62d3a388-6de6-4019-ab95-56b5e96d0891">Connecting an Interrupt Service Routine to a ParallelPort</a>.</div>
<div> </div>



## -see-also

<a href="..\parallel\nc-parallel-pparallel_set_chip_mode.md">PPARALLEL_SET_CHIP_MODE</a>



<a href="..\parallel\ni-parallel-ioctl_internal_parallel_set_chip_mode.md">IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE</a>



<a href="..\parallel\ni-parallel-ioctl_internal_parallel_connect_interrupt.md">IOCTL_INTERNAL_PARALLEL_CONNECT_INTERRUPT</a>



<a href="..\parallel\ni-parallel-ioctl_internal_parallel_clear_chip_mode.md">IOCTL_INTERNAL_PARALLEL_CLEAR_CHIP_MODE</a>



<a href="..\parallel\nc-parallel-pparallel_clear_chip_mode.md">PPARALLEL_CLEAR_CHIP_MODE</a>



<a href="..\parallel\ni-parallel-ioctl_internal_get_parallel_port_info.md">IOCTL_INTERNAL_GET_PARALLEL_PORT_INFO</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [parports\parports]:%20PARALLEL_CHIP_MODE structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

