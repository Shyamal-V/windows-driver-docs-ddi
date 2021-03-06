---
UID: NS:d3dumddi._D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES
title: "_D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES"
author: windows-driver-content
description: Used by the user-mode display driver to specify overlay plane attributes.
old-location: display\d3dddi_multiplane_overlay_attributes.htm
old-project: display
ms.assetid: 6f758785-5d7f-4d63-82c7-93ced5de3da4
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: "_D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES, D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES, D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES structure [Display Devices], d3dumddi/D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES, display.d3dddi_multiplane_overlay_attributes"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
-	D3dumddi.h
apiname:
-	D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES
---

# _D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES structure


## -description


Used by the user-mode display driver to specify overlay plane attributes.


## -syntax


````
typedef struct _D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES {
  UINT                                         Flags;
  RECT                                         SrcRect;
  RECT                                         DstRect;
#if (D3D_UMD_INTERFACE_VERSION >= D3D_UMD_INTERFACE_VERSION_WDDM1_3)
  RECT                                         ClipRect;
#endif 
  D3DDDI_ROTATION                              Rotation;
  D3DDDI_MULTIPLANE_OVERLAY_BLEND              Blend;
#if (D3D_UMD_INTERFACE_VERSION >= D3D_UMD_INTERFACE_VERSION_WDDM1_3)
  UINT                                         DirtyRectCount;
  RECT                                         *pDirtyRects;
#else 
  UINT                                         NumFilters;
  void                                         *pFilters;
#endif 
  D3DDDI_MULTIPLANE_OVERLAY_VIDEO_FRAME_FORMAT VideoFrameFormat;
  UINT                                         YCbCrFlags;
#if (D3D_UMD_INTERFACE_VERSION >= D3D_UMD_INTERFACE_VERSION_WDDM1_3)
  D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY    StretchQuality;
#endif 
} D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES;
````


## -struct-fields




### -field Flags

Specifies a flip operation as one of the applicable values in the <a href="..\d3dumddi\ne-d3dumddi-_d3dddi_multiplane_overlay_flags.md">D3DDDI_MULTIPLANE_OVERLAY_FLAGS</a> enumeration.


### -field SrcRect

Specifies the source rectangle, of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>, relative to the source resource.


### -field DstRect

Specifies the destination rectangle, of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>, relative to the monitor resolution.


### -field ClipRect

Specifies any additional clipping, of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>, relative to the <b>DstRect</b> rectangle, after the data has been stretched according to the values of <b>SrcRect</b> and <b>DstRect</b>.

The driver and hardware can use the <b>ClipRect</b> member to apply a common stretch factor as the clipping changes when an app occludes part of the <b>DstRect</b> destination rectangle.


### -field Rotation

Specifies the clockwise rotation of the overlay plane, given as a value from the <a href="..\d3dukmdt\ne-d3dukmdt-_d3dddi_rotation.md">D3DDDI_ROTATION</a> enumeration.


### -field Blend

Specifies the blend mode that applies to this overlay plane and the plane beneath it, given as a value from the <a href="..\d3dumddi\ne-d3dumddi-_d3dddi_multiplane_overlay_blend.md">D3DDDI_MULTIPLANE_OVERLAY_BLEND</a> enumeration.


### -field DirtyRectCount

The number of dirty rectangles specified for the overlay plane. If zero, the entire plane is considered dirty.


### -field pDirtyRects

A pointer to an array of dirty rectangles (<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>s), relative to the source rectangle <b>SrcRect</b>, that indicate the portion of the overlay plane that has changed.

The driver can use this member to perform optimizations, though it's not required to use the dirty rectangle info. However, the driver should never fail a function call based on the provided dirty rectangles.


### -field NumFilters

Optionally specifies the number of filters that the driver and hardware implement on the overlay plane. Note that the operating system ignores this member.


### -field pFilters

An optional pointer to a buffer that specifies the filters that the driver and hardware implement on the overlay plane. Note that the operating system ignores this member.


### -field VideoFrameFormat

Specifies the overlay plane's video frame format, given as a value from the <a href="..\d3dumddi\ne-d3dumddi-d3dddi_multiplane_overlay_video_frame_format.md">D3DDDI_MULTIPLANE_OVERLAY_VIDEO_FRAME_FORMAT</a> enumeration.

<div class="alert"><b>Note</b>  This value must always be <b>DXGI_DDI_MULIIPLANE_OVERLAY_VIDEO_FRAME_FORMAT_PROGRESSIVE</b>. The operating system does not support the other enumeration values.</div>
<div> </div>

### -field YCbCrFlags

Specifies YUV range and conversion info given as a value from the <a href="..\d3dumddi\ne-d3dumddi-d3dddi_multiplane_overlay_ycbcr_flags.md">D3DDDI_MULTIPLANE_OVERLAY_YCbCr_FLAGS</a> enumeration.


### -field StretchQuality

Specifies the overlay plane's stretch quality, given as a value from the <a href="..\d3dumddi\ne-d3dumddi-d3dddi_multiplane_overlay_stretch_quality.md">D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY</a> enumeration.


## -see-also

<a href="..\d3dumddi\ne-d3dumddi-d3dddi_multiplane_overlay_stretch_quality.md">D3DDDI_MULTIPLANE_OVERLAY_STRETCH_QUALITY</a>



<a href="..\d3dumddi\ne-d3dumddi-_d3dddi_multiplane_overlay_blend.md">D3DDDI_MULTIPLANE_OVERLAY_BLEND</a>



<a href="..\d3dukmdt\ne-d3dukmdt-_d3dddi_rotation.md">D3DDDI_ROTATION</a>



<a href="..\d3dumddi\ne-d3dumddi-_d3dddi_multiplane_overlay_flags.md">D3DDDI_MULTIPLANE_OVERLAY_FLAGS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="..\d3dumddi\ne-d3dumddi-d3dddi_multiplane_overlay_ycbcr_flags.md">D3DDDI_MULTIPLANE_OVERLAY_YCbCr_FLAGS</a>



<a href="..\d3dumddi\ne-d3dumddi-d3dddi_multiplane_overlay_video_frame_format.md">D3DDDI_MULTIPLANE_OVERLAY_VIDEO_FRAME_FORMAT</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DDDI_MULTIPLANE_OVERLAY_ATTRIBUTES structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

