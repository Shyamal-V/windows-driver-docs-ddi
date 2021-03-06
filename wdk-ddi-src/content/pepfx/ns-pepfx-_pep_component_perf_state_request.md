---
UID: NS:pepfx._PEP_COMPONENT_PERF_STATE_REQUEST
title: "_PEP_COMPONENT_PERF_STATE_REQUEST"
author: windows-driver-content
description: The PEP_COMPONENT_PERF_STATE_REQUEST structure specifies a performance state (P-state) set and a new performance level to assign to this set.
old-location: kernel\pep_component_perf_state_request.htm
old-project: kernel
ms.assetid: E34E8B3E-787D-4C6A-9F40-AD6728063AD9
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: pepfx/PEP_COMPONENT_PERF_STATE_REQUEST, PPEP_COMPONENT_PERF_STATE_REQUEST, *PPEP_COMPONENT_PERF_STATE_REQUEST, kernel.pep_component_perf_state_request, PPEP_COMPONENT_PERF_STATE_REQUEST structure pointer [Kernel-Mode Driver Architecture], PEP_COMPONENT_PERF_STATE_REQUEST structure [Kernel-Mode Driver Architecture], PEP_COMPONENT_PERF_STATE_REQUEST, _PEP_COMPONENT_PERF_STATE_REQUEST, pepfx/PPEP_COMPONENT_PERF_STATE_REQUEST
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: pepfx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 10.
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
-	pepfx.h
apiname:
-	PEP_COMPONENT_PERF_STATE_REQUEST
product: Windows
targetos: Windows
req.typenames: "*PPEP_COMPONENT_PERF_STATE_REQUEST, PEP_COMPONENT_PERF_STATE_REQUEST"
---

# _PEP_COMPONENT_PERF_STATE_REQUEST structure


## -description


The <b>PEP_COMPONENT_PERF_STATE_REQUEST</b> structure specifies a performance state (P-state) set and a new performance level to assign to this set.


## -syntax


````
typedef struct _PEP_COMPONENT_PERF_STATE_REQUEST {
  ULONG Set;
  union {
    ULONG     StateIndex;
    ULONGLONG StateValue;
  };
} PEP_COMPONENT_PERF_STATE_REQUEST, *PPEP_COMPONENT_PERF_STATE_REQUEST;
````


## -struct-fields




### -field Set

The index of the P-state set to which to assign the new performance level. If N is the number of P-state sets specified for this component, P-state set indexes range from 0 to N–1. The PEP previously specified the number of P-state sets in response to a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186839">PEP_DPM_QUERY_COMPONENT_PERF_CAPABILITIES</a> notification.


### -field StateIndex

 


### -field StateValue

 




#### - ( unnamed union )

A value that indicates the new performance level that has been selected for this P-state set.



#### StateIndex

The index of the discrete value to use as the new performance level. This member is used if the performance level for this P-state set is expressed as an index into an array of discrete values. The PEP previously supplied this array of discrete values in response to a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186842">PEP_DPM_QUERY_COMPONENT_PERF_STATES</a> notification.



#### StateValue

The value to use as the new performance level. This member is used if the performance level for this P-state set is expressed as a value in a continuous range of possible values. The PEP previously supplied this range in response to a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt186840">PEP_DPM_QUERY_COMPONENT_PERF_SET</a> notification.


## -remarks



The <b>PerfRequests</b> member of the <a href="..\pepfx\ns-pepfx-_pep_request_component_perf_state.md">PEP_REQUEST_COMPONENT_PERF_STATE</a> structure is a pointer to an array of <b>PEP_COMPONENT_PERF_STATE_REQUEST</b> structures.




## -see-also

<a href="..\pepfx\ns-pepfx-_pep_request_component_perf_state.md">PEP_REQUEST_COMPONENT_PERF_STATE</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PEP_COMPONENT_PERF_STATE_REQUEST structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

