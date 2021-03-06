---
UID: NS:wdm._PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
title: "_PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY"
author: windows-driver-content
description: The PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure describes a PCI Express (PCIe) uncorrectable error severity register of a PCIe advanced error reporting capability structure.
old-location: pci\pci_express_uncorrectable_error_severity.htm
old-project: PCI
ms.assetid: de2a908a-a032-4b61-963e-e5028ccdba11
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: wdm/PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY union [Buses], *PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, wdm/PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, pci_struct_49aec790-2c99-489c-b0ca-0653ebe5b52c.xml, PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY union pointer [Buses], PCI.pci_express_uncorrectable_error_severity, _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
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
-	PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY
product: Windows
targetos: Windows
req.typenames: "*PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY"
req.product: Windows 10 or later.
---

# _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure


## -description


The PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure describes a PCI Express (PCIe) uncorrectable error severity register of a PCIe advanced error reporting capability structure.


## -syntax


````
typedef union _PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY {
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
} PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY, *PPCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY;
````


## -struct-fields




### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.Undefined

A single bit that contains an undefined value. In versions of the <i>PCIe Specification</i> prior to version 1.1, this bit indicates that a reported link training error is a fatal error.


### -field DUMMYSTRUCTNAME.Reserved1

Reserved.


### -field DUMMYSTRUCTNAME.DataLinkProtocolError

A single bit that indicates that a reported data link protocol error is a fatal error.


### -field DUMMYSTRUCTNAME.SurpriseDownError

A single bit that indicates that a reported surprise down error is a fatal error.


### -field DUMMYSTRUCTNAME.Reserved2

Reserved.


### -field DUMMYSTRUCTNAME.PoisonedTLP

A single bit that indicates that a reported poisoned transaction layer packet (TLP) is a fatal error.


### -field DUMMYSTRUCTNAME.FlowControlProtocolError

A single bit that indicates that a reported flow control protocol error is a fatal error.


### -field DUMMYSTRUCTNAME.CompletionTimeout

A single bit that indicates that a reported completion timeout is a fatal error.


### -field DUMMYSTRUCTNAME.CompleterAbort

A single bit that indicates that a reported completer abort is a fatal error.


### -field DUMMYSTRUCTNAME.UnexpectedCompletion

A single bit that indicates that a reported unexpected completion is a fatal error.


### -field DUMMYSTRUCTNAME.ReceiverOverflow

A single bit that indicates that a reported receiver overflow is a fatal error.


### -field DUMMYSTRUCTNAME.MalformedTLP

A single bit that indicates that a reported malformed transaction layer packet (TLP) is a fatal error.


### -field DUMMYSTRUCTNAME.ECRCError

A single bit that indicates that a reported end-to-end cyclic redundancy check (ECRC) error is a fatal error.


### -field DUMMYSTRUCTNAME.UnsupportedRequestError

A single bit that indicates that a reported unsupported request error is a fatal error.


### -field DUMMYSTRUCTNAME.AcsViolation

 


### -field DUMMYSTRUCTNAME.UncorrectableInternalError

 


### -field DUMMYSTRUCTNAME.MCBlockedTlp

 


### -field DUMMYSTRUCTNAME.AtomicOpEgressBlocked

 


### -field DUMMYSTRUCTNAME.TlpPrefixBlocked

 


### -field DUMMYSTRUCTNAME.Reserved3

Reserved.


### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure.


## -remarks



The PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY structure is contained in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff537458">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structures.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537458">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [PCI\buses]:%20PCI_EXPRESS_UNCORRECTABLE_ERROR_SEVERITY union%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

