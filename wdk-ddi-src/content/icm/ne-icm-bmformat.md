---
UID: NE:icm.BMFORMAT
title: BMFORMAT
author: windows-driver-content
description: The values of the BMFORMAT enumeration are used by WCS functions to indicate the format that particular bitmaps are in. This data type is extended from BMFORMAT that is available in versions of Windows released before Windows Vista.
old-location: print\bmformat.htm
old-project: print
ms.assetid: 1c29bf1e-e785-48ab-aa2c-3665fd5c0ab0
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: BM_6CHANNEL, icm/BM_10b_Lab, BM_5CHANNEL, icm/BM_BGRTRIPLETS, icm/BM_32b_scARGB, BM_10b_G3CH, BM_R10G10B10A2_XR, icm/BM_16b_XYZ, icm/BMFORMAT, print.bmformat, BM_G3CHTRIPLETS, BM_S2DOT13FIXED_scARGB, icm/BM_GRAY, icm/BM_7CHANNEL, BM_32b_scRGB, BM_16b_Yxy, icm/BM_R10G10B10A2_XR, BM_LabTRIPLETS, icm/BM_6CHANNEL, BM_S2DOT13FIXED_scRGB, icm/BM_RGBTRIPLETS, BM_x555RGB, icm/BM_x555XYZ, BM_32b_scARGB, BM_x555Yxy, BMFORMAT, BM_xRGBQUADS, icm/BM_8CHANNEL, icm/BM_CMYKQUADS, icm/BM_565RGB, icm/BM_R16G16B16A16_FLOAT, icm/BM_x555Lab, BM_CMYKQUADS, BM_10b_Yxy, icm/BM_R10G10B10A2, icm/BM_32b_scRGB, BM_GRAY, colorfnc_44898765-c0de-41ae-8036-b288ab45b3cb.xml, icm/BM_NAMED_INDEX, BM_YxyTRIPLETS, icm/BM_10b_XYZ, icm/BM_16b_Yxy, icm/BM_x555G3CH, BM_10b_XYZ, BM_8CHANNEL, icm/BM_YxyTRIPLETS, BM_KYMCQUADS, icm/BM_10b_Yxy, icm/BM_XYZTRIPLETS, icm/BM_10b_RGB, icm/BM_xBGRQUADS, BM_10b_Lab, *PBMFORMAT, BM_NAMED_INDEX, BM_x555Lab, BM_7CHANNEL, BM_16b_Lab, BM_R16G16B16A16_FLOAT, icm/BM_S2DOT13FIXED_scRGB, BM_16b_GRAY, icm/BM_G3CHTRIPLETS, BM_BGRTRIPLETS, icm/BM_16b_RGB, icm/BM_5CHANNEL, icm/BM_x555RGB, BM_RGBTRIPLETS, icm/BM_xG3CHQUADS, BM_16b_XYZ, icm/BM_16b_Lab, BM_x555G3CH, BM_10b_RGB, BM_xBGRQUADS, icm/BM_10b_G3CH, BMFORMAT enumeration [Print Devices], BM_565RGB, BM_XYZTRIPLETS, icm/BM_LabTRIPLETS, BM_16b_RGB, icm/BM_xRGBQUADS, BM_x555XYZ, BM_xG3CHQUADS, icm/BM_16b_GRAY, icm/BM_S2DOT13FIXED_scARGB, icm/BM_16b_G3CH, icm/BM_KYMCQUADS, BM_R10G10B10A2, BM_16b_G3CH, icm/BM_x555Yxy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Included in Windows Vista and later.
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
-	icm.h
apiname:
-	BMFORMAT
product: Windows
targetos: Windows
req.typenames: BMFORMAT
---

# BMFORMAT enumeration


## -description


The values of the BMFORMAT enumeration are used by WCS functions to indicate the format that particular bitmaps are in. This data type is extended from BMFORMAT that is available in versions of Windows released before Windows Vista.


## -syntax


````
typedef enum  { 
  BM_x555RGB              = 0x0000,
  BM_x555XYZ              = 0x0101,
  BM_x555Yxy              = 0x102,
  BM_x555Lab              = 0x103,
  BM_x555G3CH             = 0x104,
  BM_RGBTRIPLETS          = 0x0002,
  BM_BGRTRIPLETS          = 0x0004,
  BM_XYZTRIPLETS          = 0x0201,
  BM_YxyTRIPLETS          = 0x202,
  BM_LabTRIPLETS          = 0x203,
  BM_G3CHTRIPLETS         = 0x204,
  BM_5CHANNEL             = 0x205,
  BM_6CHANNEL             = 0x206,
  BM_7CHANNEL             = 0x207,
  BM_8CHANNEL             = 0x208,
  BM_GRAY                 = 0x209,
  BM_xRGBQUADS            = 0x0008,
  BM_xBGRQUADS            = 0x0010,
  BM_xG3CHQUADS           = 0x0304,
  BM_KYMCQUADS            = 0x305,
  BM_CMYKQUADS            = 0x0020,
  BM_10b_RGB              = 0x0009,
  BM_10b_XYZ              = 0x0401,
  BM_10b_Yxy              = 0x402,
  BM_10b_Lab              = 0x403,
  BM_10b_G3CH             = 0x404,
  BM_NAMED_INDEX          = 0x405,
  BM_16b_RGB              = 0x000A,
  BM_16b_XYZ              = 0x0501,
  BM_16b_Yxy              = 0x502,
  BM_16b_Lab              = 0x503,
  BM_16b_G3CH             = 0x504,
  BM_16b_GRAY             = 0x505,
  BM_565RGB               = 0x0001,
  BM_32b_scRGB            = 0x0601,
  BM_32b_scARGB           = 0x0602,
  BM_S2DOT13FIXED_scRGB   = 0x0603,
  BM_S2DOT13FIXED_scARGB  = 0x0604,
  BM_R10G10B10A2          = 0x0701,
  BM_R10G10B10A2_XR       = 0x0702,
  BM_R16G16B16A16_FLOAT   = 0x0703 
} BMFORMAT;
````


## -enum-fields




### -field BM_x555RGB

16 bits per pixel. RGB color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_x555XYZ

16 bits per pixel. Yxy color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_x555Yxy

16 bits per pixel. Yxy color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_x555Lab

BM_x555G3CH


### -field BM_x555G3CH

16 bits per pixel. G3CH color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_RGBTRIPLETS

24 bits per pixel maximum. For three channel colors, such as red, green, and blue, the total size is 24 bits per pixel. For single channel colors, such as gray, the total size is 8 bits per pixel.


### -field BM_BGRTRIPLETS

24 bits per pixel maximum. For three channel colors, such as red, green, and blue, the total size is 24 bits per pixel. For single channel colors, such as gray, the total size is 8 bits per pixel.


### -field BM_XYZTRIPLETS

24 bits per pixel maximum. For three channel colors, such as red, green, and blue, the total size is 24 bits per pixel. For single channel colors, such as gray, the total size is 8 bits per pixel.


### -field BM_YxyTRIPLETS

24 bits per pixel maximum. For three channel, Y, x, and y values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.


### -field BM_LabTRIPLETS

24 bits per pixel maximum. For three channel, L, a, and b values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.


### -field BM_G3CHTRIPLETS

24 bits per pixel maximum. For three channel values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.


### -field BM_5CHANNEL

40 bits per pixel. 8 bits apiece are used for each channel.


### -field BM_6CHANNEL


### -field BM_7CHANNEL

56 bits per pixel. 8 bits apiece are used for each channel.


### -field BM_8CHANNEL

64 bits per pixel. 8 bits apiece are used for each channel.


### -field BM_GRAY

32 bits per pixel. Only the 8 bit gray-scale value is used.


### -field BM_xRGBQUADS

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.


### -field BM_xBGRQUADS

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.


### -field BM_xG3CHQUADS

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.


### -field BM_KYMCQUADS

32 bits per pixel. 8 bits are used for each color channel.


### -field BM_CMYKQUADS

32 bits per pixel. 8 bits are used for each color channel.


### -field BM_10b_RGB

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored. 


### -field BM_10b_XYZ

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_10b_Yxy

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_10b_Lab

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_10b_G3CH

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_NAMED_INDEX

32 bits per pixel. Named color indices. Index numbering begins at one. 


### -field BM_16b_RGB

64 bits per pixel. 16 bits are used for the gray-scale value. Each of the three color channels uses 16 bits.


### -field BM_16b_XYZ

64 bits per pixel. 16 bits are used for the gray-scale value. Each of the three color channels uses 16 bits.


### -field BM_16b_Yxy

64 bits per pixel. 16 bits are used for the gray-scale value. Each of the three color channels uses 16 bits.


### -field BM_16b_Lab

64 bits per pixel. 16 bits are used for the gray-scale value. Each of the three color channels uses 16 bits.


### -field BM_16b_G3CH

64 bits per pixel. 16 bits are used for the gray-scale value. Each of the three color channels uses 16 bits.


### -field BM_16b_GRAY

64 bits per pixel. 16 bits are used for the gray-scale value. All other bits are ignored.


### -field BM_565RGB

16 bits per pixel. 5 bits are used for red, 6 for green, and 5 for blue.


### -field BM_32b_scRGB

96 bits per pixel. 32 bits are used for each color channel, as defined by the IEEE 32-bit floating point standard.


### -field BM_32b_scARGB

128 bits per pixel. 32 bits are used for each color channel, as defined by the IEEE 32-bit floating point standard.


### -field BM_S2DOT13FIXED_scRGB

48 bits per pixel. Color data is stored as one 16-bit word per channel, with a fixed range of -4 to +4, inclusive. A signed format is used, with 1 bit for the sign, 2 bits for the integer portion, and 13 bits for the fractional portion.


### -field BM_S2DOT13FIXED_scARGB

64 bits per pixel. Color data is stored as one 16-bit word per channel, with a fixed range of -4 to +4, inclusive. A signed format is used, with 1 bit for the sign, 2 bits for the integer portion, and 13 bits for the fractional portion.


### -field BM_R10G10B10A2


### -field BM_R10G10B10A2_XR


### -field BM_R16G16B16A16_FLOAT

#endif // NTDDI_VERSION &gt;= NTDDI_WIN7


## -remarks



The last four values were added to the BMFORMAT enumeration beginning with Windows Vista.

The PBMFORMAT and LPBMFORMAT data types are defined as pointers to this enumeration:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef BMFORMAT *PBMFORMAT, *LPBMFORMAT;</pre>
</td>
</tr>
</table></span></div>


