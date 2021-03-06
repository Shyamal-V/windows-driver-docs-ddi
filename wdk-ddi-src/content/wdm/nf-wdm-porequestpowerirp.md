---
UID: NF:wdm.PoRequestPowerIrp
title: PoRequestPowerIrp function
author: windows-driver-content
description: The PoRequestPowerIrp routine allocates a power IRP and sends it to the top driver in the device stack for the specified device.
old-location: kernel\porequestpowerirp.htm
old-project: kernel
ms.assetid: 99330348-bcc2-4a89-96f8-e1b67d9ebe25
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: PoRequestPowerIrp, wdm/PoRequestPowerIrp, PoRequestPowerIrp routine [Kernel-Mode Driver Architecture], kernel.porequestpowerirp, portn_d417d88c-2f6d-4af9-b7de-455dfcc1b9df.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: MarkDevicePower, PowerDownFail, PowerUpFail, RequestedPowerIrp, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: "<= DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	DllExport
apilocation:
-	NtosKrnl.exe
apiname:
-	PoRequestPowerIrp
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# PoRequestPowerIrp function


## -description


The <b>PoRequestPowerIrp</b> routine allocates a power <a href="..\wdm\ns-wdm-_irp.md">IRP</a> and sends it to the top driver in the device stack for the specified device.


## -syntax


````
NTSTATUS PoRequestPowerIrp(
  _In_     PDEVICE_OBJECT          DeviceObject,
  _In_     UCHAR                   MinorFunction,
  _In_     POWER_STATE             PowerState,
  _In_opt_ PREQUEST_POWER_COMPLETE CompletionFunction,
  _In_opt_ PVOID                   Context,
  _Out_    PIRP                    *Irp
);
````


## -parameters




### -param DeviceObject [in]

A pointer to the target <a href="..\wdm\ns-wdm-_device_object.md">DEVICE_OBJECT</a> for the IRP. In Windows 2000 and later versions of Windows, this parameter can point to a physical device object (<a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDO</a>) or a functional device object (<a href="https://msdn.microsoft.com/f697e0db-1db0-4a81-94d8-0ca079885480">FDO</a>). In Windows 98/Me, this parameter must point to the PDO of the underlying device.


### -param MinorFunction [in]

Specifies one of the following minor power IRP codes: <a href="https://msdn.microsoft.com/library/windows/hardware/ff551699">IRP_MN_QUERY_POWER</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff551744">IRP_MN_SET_POWER</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/ff551766">IRP_MN_WAIT_WAKE</a>.


### -param PowerState [in]

Specifies a <a href="..\wdm\ns-wdm-_power_state.md">POWER_STATE</a> value to pass in the IRP. For <b>IRP_MN_SET_POWER</b> and <b>IRP_MN_QUERY_POWER</b>, specify the requested new <a href="https://msdn.microsoft.com/2229f34c-9b88-4e3e-802e-f7be2c7ef168">device power state</a>. Possible values are <a href="..\wudfddi\ne-wudfddi-_device_power_state.md">DEVICE_POWER_STATE</a> values.

For <b>IRP_MN_WAIT_WAKE</b>, specify the lowest (least-powered) <a href="https://msdn.microsoft.com/bb30bc89-d1f2-4cb3-bcfb-fb76c69dba27">system power state</a> from which the device should be allowed to wake the system. Possible values are <a href="..\wdm\ne-wdm-_system_power_state.md">SYSTEM_POWER_STATE</a> values.


### -param CompletionFunction [in, optional]

A pointer to the caller's <a href="https://msdn.microsoft.com/library/windows/hardware/ff961906">PowerCompletion</a> callback routine. The I/O manager calls this routine when the IRP has completed. This parameter is optional and can be set to <b>NULL</b> if no <i>PowerCompletion</i> callback routine is needed.


### -param Context [in, optional]

A pointer to a caller-supplied context to be passed through to the <i>PowerCompletion</i> callback. When the caller requests a device set-power IRP in response to a system set-power IRP, <i>Context</i> should contain the system set-power IRP that triggered the request.


### -param Irp [out]

A pointer to a caller-supplied variable in which <b>PoRequestPowerIrp</b> returns a pointer to the IRP that it allocates. Specify a value for <i>Irp</i> only if the <i>MinorFunction</i> parameter is set to <b>IRP_MN_WAIT_WAKE</b>. Otherwise, this parameter should always be <b>NULL</b> because the IRP might be completed before <b>PoRequestPowerIrp</b> returns, causing this parameter to point to memory that has already been discarded.


## -returns



<b>PoRequestPowerIrp</b> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The IRP has been sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The routine could not allocate the IRP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER_2</b></dt>
</dl>
</td>
<td width="60%">
<i>MinorFunction</i> does not signify a valid minor power IRP code.

</td>
</tr>
</table>
 




## -remarks



A device power policy owner calls this routine to send a wait/wake, query, or set-power IRP.

A driver calls <b>PoRequestPowerIrp</b>—not <a href="..\wdm\nf-wdm-ioallocateirp.md">IoAllocateIrp</a>—to allocate and send a power IRP that has minor IRP code <b>IRP_MN_SET_POWER</b>, <b>IRP_MN_QUERY_POWER</b>, or <b>IRP_MN_WAIT_WAKE</b>. (A driver must call <b>IoAllocateIrp</b> to send a power IRP with minor IRP code <a href="https://msdn.microsoft.com/library/windows/hardware/ff551644">IRP_MN_POWER_SEQUENCE</a>.) 

If <b>PoRequestPowerIrp</b> returns a status value of STATUS_PENDING, the routine successfully allocated a device power IRP and sent it to the top of the device stack for the device. After the bus driver and all other drivers have completed the IRP, and the I/O manager has called all <a href="..\wdm\nc-wdm-io_completion_routine.md">IoCompletion</a> routines set by drivers as they passed the IRP down the device stack, the I/O manager calls the <a href="https://msdn.microsoft.com/library/windows/hardware/ff961906">PowerCompletion</a> routine and passes to this routine the specified <i>Context</i> value. If <b>PoRequestPowerIrp</b> returns a status other than STATUS_PENDING, the routine did not send a device power IRP and the <i>PowerCompletion</i> routine is not called.

The <i>PowerCompletion</i> routine performs any additional tasks the sender of the IRP requires after all other drivers have completed the IRP. It need not free the IRP; the power manager does that. In Windows 2000 and later versions of Windows, the <i>PowerCompletion</i> routine can be called at IRQL = PASSIVE_LEVEL or IRQL = DISPATCH_LEVEL. In Windows 98/Me, the <i>PowerCompletion</i> routine is always called at IRQL = PASSIVE_LEVEL, and drivers must complete IRPs at IRQL = PASSIVE_LEVEL.

A device power policy owner calls <b>PoRequestPowerIrp</b> to send a device query- or set-power IRP when it receives a system query- or set-power IRP. The driver should set an <i>IoCompletion</i> routine in the system IRP and pass the system IRP to the next lower driver. The <i>IoCompletion</i> routine calls <b>PoRequestPowerIrp</b> to send the device IRP, passing the system IRP in the <i>Context</i> parameter. The <i>Context</i> parameter is subsequently passed to the <i>PowerCompletion</i> routine for the device IRP. In the <i>PowerCompletion</i> routine, the driver can complete the system IRP. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563731">Sending IRP_MN_QUERY_POWER or IRP_MN_SET_POWER for Device Power States</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff565599">Wait/Wake Callback Routines</a>.

Drivers can use the returned <i>Irp</i> to cancel an <b>IRP_MN_WAIT_WAKE</b> IRP. Drivers that are requesting other types of power IRPs must pass <b>NULL</b> for this parameter.




## -see-also

<a href="..\wdm\ns-wdm-_irp.md">IRP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551766">IRP_MN_WAIT_WAKE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551744">IRP_MN_SET_POWER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff961906">PowerCompletion</a>



<a href="..\wdm\nf-wdm-postartnextpowerirp.md">PoStartNextPowerIrp</a>



<a href="..\wdm\ns-wdm-_io_status_block.md">IO_STATUS_BLOCK</a>



<a href="..\wdm\nf-wdm-ioallocateirp.md">IoAllocateIrp</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551699">IRP_MN_QUERY_POWER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551644">IRP_MN_POWER_SEQUENCE</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PoRequestPowerIrp routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

