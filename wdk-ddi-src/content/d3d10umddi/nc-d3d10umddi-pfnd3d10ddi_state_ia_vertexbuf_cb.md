---
UID: NC:d3d10umddi.PFND3D10DDI_STATE_IA_VERTEXBUF_CB
title: PFND3D10DDI_STATE_IA_VERTEXBUF_CB
author: windows-driver-content
description: The pfnStateIaVertexBufCb function causes the Microsoft Direct3D 10 runtime to refresh the set of vertex buffers that are bound to the input assembler.
old-location: display\pfnstateiavertexbufcb.htm
old-project: display
ms.assetid: 15068932-b769-4027-986f-195b569a23eb
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.pfnstateiavertexbufcb, pfnStateIaVertexBufCb callback function [Display Devices], pfnStateIaVertexBufCb, PFND3D10DDI_STATE_IA_VERTEXBUF_CB, PFND3D10DDI_STATE_IA_VERTEXBUF_CB, d3d10umddi/pfnStateIaVertexBufCb, d3d10state_functions_b08135a0-2a61-4823-9153-bf89ea24e0fa.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
-	UserDefined
apilocation:
-	d3d10umddi.h
apiname:
-	pfnStateIaVertexBufCb
product: Windows
targetos: Windows
req.typenames: "*PSETRESULT_INFO, SETRESULT_INFO"
---

# PFND3D10DDI_STATE_IA_VERTEXBUF_CB callback


## -description


The <b>pfnStateIaVertexBufCb</b> function causes the Microsoft Direct3D 10 runtime to refresh the set of vertex buffers that are bound to the input assembler.


## -prototype


````
PFND3D10DDI_STATE_IA_VERTEXBUF_CB pfnStateIaVertexBufCb;

void APIENTRY pfnStateIaVertexBufCb(
  _In_ D3D10DDI_HRTCORELAYER hRuntimeDevice,
  _In_ UINT                  Base,
  _In_ UINT                  Count
)
{ ... }
````


## -parameters




### -param D3D10DDI_HRTCORELAYER


### -param UINT








#### - Base [in]

 The beginning vertex buffer for which the runtime should refresh state. 


#### - Count [in]

 The total number of vertex buffers. The number can be -1, which specifies that the Direct3D runtime will use its high watermarks to substitute an optimal value (which is typically less than the maximum valid value for <i>Count</i>). However, no non-NULL binding exists in a slot larger than the optimal <i>Count</i> value.


#### - hRuntimeDevice [in]

 A handle to a context for the core Direct3D 10 runtime. This handle is supplied to the driver in a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a> function. 


## -returns



None




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_corelayer_devicecallbacks.md">D3D10DDI_CORELAYER_DEVICECALLBACKS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3D10DDI_STATE_IA_VERTEXBUF_CB callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

