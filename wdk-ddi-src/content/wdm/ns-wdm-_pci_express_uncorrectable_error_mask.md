---
UID: NS:wdm._PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK
title: "_PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK"
author: windows-driver-content
description: The PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK structure describes a PCI Express (PCIe) uncorrectable error mask register of a PCIe advanced error reporting capability structure.
old-location: pci\pci_express_uncorrectable_error_mask.htm
old-project: PCI
ms.assetid: 0dfc6e49-5556-4163-abef-b00a26a7a2ad
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: PCI.pci_express_uncorrectable_error_mask, PPCI_EXPRESS_UNCORRECTABLE_ERROR_MASK union pointer [Buses], *PPCI_EXPRESS_UNCORRECTABLE_ERROR_MASK, _PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK, wdm/PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK, PPCI_EXPRESS_UNCORRECTABLE_ERROR_MASK, wdm/PPCI_EXPRESS_UNCORRECTABLE_ERROR_MASK, pci_struct_309db853-f6d7-4f88-9a73-861d63a1e927.xml, PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK union [Buses], PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h
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
req.irql: PASSIVE_LEVEL (see Remarks section)
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	wdm.h
apiname:
-	PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK
product: Windows
targetos: Windows
req.typenames: "*PPCI_EXPRESS_UNCORRECTABLE_ERROR_MASK, PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK"
req.product: Windows 10 or later.
---

# _PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK structure


## -description


The PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK structure describes a PCI Express (PCIe) uncorrectable error mask register of a PCIe advanced error reporting capability structure.


## -syntax


````
typedef union _PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK {
  struct {
    ULONG Undefined  :1;
    ULONG Reserved1  :3;
    ULONG DataLinkProtocolError  :1;
    ULONG SurpriseDownError  :1;
    ULONG Reserved2  :6;
    ULONG PoisonedTLP  :1;
    ULONG FlowControlProtocolError  :1;
    ULONG CompletionTimeout  :1;
    ULONG CompleterAbort  :1;
    ULONG UnexpectedCompletion  :1;
    ULONG ReceiverOverflow  :1;
    ULONG MalformedTLP  :1;
    ULONG ECRCError  :1;
    ULONG UnsupportedRequestError  :1;
    ULONG Reserved3  :11;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK, *PPCI_EXPRESS_UNCORRECTABLE_ERROR_MASK;
````


## -struct-fields




### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.Undefined

A single bit that contains an undefined value. In versions of the <i>PCIe Specification</i> prior to version 1.1, this bit indicates that the reporting of link training errors is masked.


### -field DUMMYSTRUCTNAME.Reserved1

Reserved.


### -field DUMMYSTRUCTNAME.DataLinkProtocolError

A single bit that indicates that the reporting of data link protocol errors is masked.


### -field DUMMYSTRUCTNAME.SurpriseDownError

A single bit that indicates that the reporting of surprise down errors is masked.


### -field DUMMYSTRUCTNAME.Reserved2

Reserved.


### -field DUMMYSTRUCTNAME.PoisonedTLP

A single bit that indicates that the reporting of poisoned transaction layer packets (TLPs) is masked.


### -field DUMMYSTRUCTNAME.FlowControlProtocolError

A single bit that indicates that the reporting of flow control protocol errors is masked.


### -field DUMMYSTRUCTNAME.CompletionTimeout

A single bit that indicates that the reporting of completion timeouts is masked.


### -field DUMMYSTRUCTNAME.CompleterAbort

A single bit that indicates that the reporting of completer aborts is masked.


### -field DUMMYSTRUCTNAME.UnexpectedCompletion

A single bit that indicates that the reporting of unexpected completions is masked.


### -field DUMMYSTRUCTNAME.ReceiverOverflow

A single bit that indicates that the reporting of receiver overflows is masked.


### -field DUMMYSTRUCTNAME.MalformedTLP

A single bit that indicates that the reporting of malformed transaction layer packets (TLPs) is masked.


### -field DUMMYSTRUCTNAME.ECRCError

A single bit that indicates that the reporting of end-to-end cyclic redundancy check (ECRC) errors is masked.


### -field DUMMYSTRUCTNAME.UnsupportedRequestError

A single bit that indicates that the reporting of unsupported request errors is masked.


### -field DUMMYSTRUCTNAME.AcsViolation

 


### -field DUMMYSTRUCTNAME.UncorrectableInternalError

 


### -field DUMMYSTRUCTNAME.MCBlockedTlp

 


### -field DUMMYSTRUCTNAME.AtomicOpEgressBlocked

 


### -field DUMMYSTRUCTNAME.TlpPrefixBlocked

 


### -field DUMMYSTRUCTNAME.Reserved3

Reserved.


### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK structure.


## -remarks



The PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK structure is contained in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff537458">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structures.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537458">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [PCI\buses]:%20PCI_EXPRESS_UNCORRECTABLE_ERROR_MASK union%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

