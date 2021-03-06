---
UID: NC:storport.HW_INITIALIZE
title: HW_INITIALIZE
author: windows-driver-content
description: The HwStorInitialize routine initializes the miniport driver after a system reboot or power failure occurs.
old-location: storage\hwstorinitialize.htm
old-project: storage
ms.assetid: c6c70f15-2614-4623-8979-6046cdc6239b
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: storage.hwstorinitialize, HwStorInitialize routine [Storage Devices], HwStorInitialize, HW_INITIALIZE, HW_INITIALIZE, storport/HwStorInitialize, stormini_ef5f6b0d-443d-4ee4-a319-117e5be40831.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
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
req.irql: DIRQL (See Remarks section.)
topictype:
-	APIRef
-	kbSyntax
apitype:
-	UserDefined
apilocation:
-	Storport.h
apiname:
-	HwStorInitialize
product: Windows
targetos: Windows
req.typenames: STORAGE_DEVICE_UNIQUE_IDENTIFIER, *PSTORAGE_DEVICE_UNIQUE_IDENTIFIER
req.product: Windows 10 or later.
---

# HW_INITIALIZE callback


## -description


The <b>HwStorInitialize</b> routine initializes the miniport driver after a system reboot or power failure occurs. It is called by StorPort after <a href="..\storport\nc-storport-hw_find_adapter.md">HwStorFindAdapter</a> successfully returns. <b>HwStorInitialize</b> initializes the HBA and finds all devices that are of interest to the miniport driver.


## -prototype


````
HW_INITIALIZE HwStorInitialize;

BOOLEAN HwStorInitialize(
   IN PVOID DeviceExtension
)
{ ... }
````


## -parameters




### -param DeviceExtension

A pointer to the miniport driver's per HBA storage area. 


## -returns



If the initialization succeeds, <b>HwStorInitialize</b> returns <b>TRUE</b>. 




## -remarks



The name <b>HwStorInitialize</b> is just a placeholder. The actual prototype of this routine is defined in <i>Storport.h</i> as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef
BOOLEAN
HW_INITIALIZE (
  _In_ PVOID  DeviceExtension
  );</pre>
</td>
</tr>
</table></span></div>
Because <b>HwStorInitialize</b> is called at DIRQL, as much of the initialization process as possible should be performed by <a href="..\storport\nc-storport-hw_passive_initialize_routine.md">HwStorPassiveInitializeRoutine</a>. If so, you must enable the passive initialization routine via <a href="..\storport\nf-storport-storportenablepassiveinitialization.md">StorPortEnablePassiveInitialization</a>. 

If interrupts are generated by the hardware initialization, the <a href="..\storport\nc-storport-hw_interrupt.md">HwStorInterrupt</a> routine will be called. In this case, the <b>HwStorInitialize</b> routine should set up any data that <b>HwStorInterrupt</b> expects (including a <a href="..\storport\nc-storport-hw_dpc_routine.md">HwStorDpcRoutine</a>, if one is used) before it begins to initialize the hardware. 

The following responsibilities are shared between <b>HwStorInitialize</b> and <a href="..\storport\nc-storport-hw_passive_initialize_routine.md">HwStorPassiveInitializeRoutine</a>:

<ul>
<li>
Initialize hardware for the HBA registers and buffers.

</li>
<li>
Initialize and allocate all <i>DeviceExtension</i> fields.

</li>
<li>
Set up and initialize all events and DPCs that are used by the miniport driver.

</li>
</ul>

#### Examples

To define an <b>HwStorInitialize</b> callback function, you must first provide a function declaration that identifies the type of callback function you’re defining. Windows provides a set of callback function types for drivers. Declaring a function using the callback function types helps <a href="https://msdn.microsoft.com/2F3549EF-B50F-455A-BDC7-1F67782B8DCA">Code Analysis for Drivers</a>, <a href="https://msdn.microsoft.com/74feeb16-387c-4796-987a-aff3fb79b556">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it’s a requirement for writing drivers for the Windows operating system.

 For example, to define a <b>HwStorInitialize</b> callback routine that is named <i>MyHwInitialize</i>, use the <b>HW_INITIALIZE</b> type as shown in this code example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HW_INITIALIZE MyHwInitialize;</pre>
</td>
</tr>
</table></span></div>
Then, implement your callback routine as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>_Use_decl_annotations_
BOOLEAN 
  MyHwInitialize( _In_ PVOID DeviceExtension )
  {
      ...
  }</pre>
</td>
</tr>
</table></span></div>
The <b>HW_INITIALIZE</b> function type is defined in the Storport.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition. The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the <b>HW_INITIALIZE</b> function type in the header file are used. For more information about the requirements for function declarations, see <a href="https://msdn.microsoft.com/40BD11CD-A559-4F90-BF39-4ED2FB800392">Declaring Functions Using Function Role Types for Storport Drivers</a>. For information about _Use_decl_annotations_, see <a href="https://msdn.microsoft.com/en-us/library/jj159529.aspx">Annotating Function Behavior</a>.




## -see-also

<a href="..\storport\nc-storport-hw_dpc_routine.md">HwStorDpcRoutine</a>



<a href="..\storport\nc-storport-hw_find_adapter.md">HwStorFindAdapter</a>



<a href="..\storport\nc-storport-hw_interrupt.md">HwStorInterrupt</a>



<a href="..\storport\nc-storport-hw_passive_initialize_routine.md">HwStorPassiveInitializeRoutine</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20HW_INITIALIZE routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

