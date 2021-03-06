---
UID: NC:iddcx.EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT
title: EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT
author: windows-driver-content
description: EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT is called by the OS to destroy an OPM protected output context.
old-location: display\evt_idd_cx_monitor_opm_destroy_protected_output.htm
old-project: display
ms.assetid: 86bd815f-b413-4680-9679-8778a47a0e27
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.evt_idd_cx_monitor_opm_destroy_protected_output, EvtIddCxMonitorOpmDestroyProtectedOutput callback function [Display Devices], EvtIddCxMonitorOpmDestroyProtectedOutput, EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT, EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT, iddcx/EvtIddCxMonitorOpmDestroyProtectedOutput, PFN_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT callback function pointer [Display Devices], PFN_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: iddcx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.irql: "_requires_same_"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	UserDefined
apilocation:
-	iddcx.h
apiname:
-	PFN_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT
product: Windows
targetos: Windows
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
---

# EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT callback


## -description


<b>EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT</b> is called by the OS to destroy an OPM protected output context.


## -prototype


````
EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT EvtIddCxMonitorOpmDestroyProtectedOutput;

NTSTATUS EvtIddCxMonitorOpmDestroyProtectedOutput(
  _In_ IDDCX_OPMCTX OpmCxtObject
)
{ ... }

typedef EVT_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT PFN_IDD_CX_MONITOR_OPM_DESTROY_PROTECTED_OUTPUT;
````


## -parameters




### -param OpmCxtObject [in]


                    
                The object for the OPM context that will be destroyed.


## -returns




(NTSTATUS) If the operation is successful, the callback function must return STATUS_SUCCESS, or another status value for which NT_SUCCESS(status) equals TRUE. Otherwise, an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code. 
                    



