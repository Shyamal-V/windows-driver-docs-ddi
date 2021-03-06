---
UID: NF:ntddk.IoSetMasterIrpStatus
title: IoSetMasterIrpStatus function
author: windows-driver-content
description: The IoSetMasterIrpStatus routine conditionally replaces the Status value in an IRP with the specified NTSTATUS value.
old-location: kernel\iosetmasterirpstatus.htm
old-project: kernel
ms.assetid: 68C7C46B-AFDB-449D-99B5-1F9A5A9AFFA4
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: IoSetMasterIrpStatus routine [Kernel-Mode Driver Architecture], kernel.iosetmasterirpstatus, IoSetMasterIrpStatus, ntddk/IoSetMasterIrpStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntddk.h
req.include-header: Ntddk.h, Ntifs.h
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: Any level.
topictype:
-	APIRef
-	kbSyntax
apitype:
-	DllExport
apilocation:
-	NtosKrnl.exe
apiname:
-	IoSetMasterIrpStatus
product: Windows
targetos: Windows
req.typenames: "*PWHEA_RAW_DATA_FORMAT, WHEA_RAW_DATA_FORMAT"
---

# IoSetMasterIrpStatus function


## -description


The <b>IoSetMasterIrpStatus</b> routine conditionally replaces the <b>Status</b> value in an IRP with the specified NTSTATUS value.


## -syntax


````
VOID IoSetMasterIrpStatus(
  _Inout_ PIRP     MasterIrp,
  _In_    NTSTATUS Status
);
````


## -parameters




### -param MasterIrp [in, out]

A pointer to the master <a href="..\wdm\ns-wdm-_irp.md">IRP</a>. For more information, see Remarks.


### -param Status [in]

An NTSTATUS value to compare to the <b>Status</b> member of the <a href="https://msdn.microsoft.com/59147bd1-6cd7-4fbe-b7bc-52e09ab88576">I/O status block</a> in the master IRP.


## -returns



None.




## -remarks



On receipt of an IRP, a driver can create two or more subordinate IRPs to perform the work requested by the original (or master) IRP. When the subordinate IRPs complete, the driver gathers the completion status codes from the subordinate IRPs and merges them to form a single completion status code for the master IRP.

<b>IoSetMasterIrpStatus</b> implements a uniform policy for merging the status codes from multiple subordinate IRPs into a status code for a master IRP. For example, if a master IRP is split into two subordinate IRPs, and one of these subordinate IRPs succeeds and the other fails, the status code from the failing IRP is used as the status code for the master IRP. However, if both subordinate IRPs fail, the more severe failure code is used as the status for the master IRP.

Before the first call to <b>IoSetMasterIrpStatus</b>, the driver sets the <b>IoStatus.Status</b> member in the master IRP to STATUS_SUCCESS (or to STATUS_FT_READ_FROM_COPY in case it is expected). Next, as each subordinate IRP completes, the driver calls <b>IoSetMasterIrpStatus</b> to merge the status code from this IRP with the status code in the master IRP. In this call, the <i>PIRP</i> parameter points to the master IRP, and the <i>Status</i> parameter is set to the value of the <b>IoStatus.Status</b> member in the subordinate IRP.

As a general rule, <b>IoSetMasterIrpStatus</b> replaces the status code in <i>PIRP</i>-&gt;<b>IoStatus.Status</b> with the <i>Status</i> value in the following cases:

<ul>
<li>The status value in *<i>PIRP</i> is STATUS_SUCCESS, and <i>Status</i> is an error code.</li>
<li>The status value in *<i>PIRP</i> is an error code, but <i>Status</i> is a more severe error code.</li>
</ul>
There are two exceptions to the general rule. A <i>Status</i> value of STATUS_VERIFY_REQUIRED <u>always</u> replaces the status value in *<i>PIRP</i>. A <i>Status</i> value of STATUS_FT_READ_FROM_COPY <u>never</u> replaces the status value in *<i>PIRP</i>.




## -see-also

<a href="..\wdm\ns-wdm-_irp.md">IRP</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IoSetMasterIrpStatus routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

