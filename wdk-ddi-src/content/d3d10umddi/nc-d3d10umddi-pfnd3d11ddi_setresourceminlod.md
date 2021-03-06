---
UID: NC:d3d10umddi.PFND3D11DDI_SETRESOURCEMINLOD
title: PFND3D11DDI_SETRESOURCEMINLOD
author: windows-driver-content
description: The SetResourceMinLOD function sets the minimum level of detail (LOD) for a resource.
old-location: display\setresourceminlod.htm
old-project: display
ms.assetid: a54b2fa7-c0c2-42b7-ae89-7984282d4af4
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.setresourceminlod, SetResourceMinLOD callback function [Display Devices], SetResourceMinLOD, PFND3D11DDI_SETRESOURCEMINLOD, PFND3D11DDI_SETRESOURCEMINLOD, d3d10umddi/SetResourceMinLOD, UserModeDisplayDriverDx11_Functions_3c56a9a6-a13e-4377-a997-e84af3ff12ef.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: SetResourceMinLOD is supported beginning with the Windows 7 operating system.
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
-	SetResourceMinLOD
product: Windows
targetos: Windows
req.typenames: "*PSETRESULT_INFO, SETRESULT_INFO"
---

# PFND3D11DDI_SETRESOURCEMINLOD callback


## -description


The <i>SetResourceMinLOD</i> function sets the minimum level of detail (LOD) for a resource. 


## -prototype


````
PFND3D11DDI_SETRESOURCEMINLOD SetResourceMinLOD;

VOID APIENTRY SetResourceMinLOD(
  _In_ D3D10DDI_HDEVICE   hDevice,
  _In_ D3D10DDI_HRESOURCE hResource,
  _In_ FLOAT              MinLOD
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param D3D10DDI_HRESOURCE


### -param FLOAT








#### - MinLOD [in]

 A single-precision float vector to set for the minimum level of detail (LOD) for the resource. 


#### - hDevice [in]

 A handle to the display device (graphics context).


#### - hResource [in]

 A handle to the driver's private data for the resource. 


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the following Remarks section.




## -remarks



The driver should not encounter any error, except for D3DDDIERR_DEVICEREMOVED. Therefore, if the driver passes any error, except for D3DDDIERR_DEVICEREMOVED, in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function, the Direct3D runtime determines that the error is critical. Even if the device is removed, the driver is not required to return D3DDDIERR_DEVICEREMOVED; however, if device removal interferes with the operation of <i>SetResourceMinLOD</i> (which typically should not happen), the driver can return D3DDDIERR_DEVICEREMOVED.

The Direct3D runtime calls the driver's <i>SetResourceMinLOD</i> function to set the minimum LOD (that is, the lowest MIP map) that a shader can sample from. This minimum LOD is ignored for some operations like for the operation that the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_resourcecopy.md">ResourceCopy</a> function performs. 




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_devicefuncs.md">D3D11DDI_DEVICEFUNCS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3D11DDI_SETRESOURCEMINLOD callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

