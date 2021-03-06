---
UID: NF:wudfddi.IWDFIoRequest.GetReadParameters
title: IWDFIoRequest::GetReadParameters method
author: windows-driver-content
description: The GetReadParameters method retrieves the request parameters for a read-type request.
old-location: wdf\iwdfiorequest_getreadparameters.htm
old-project: wdf
ms.assetid: 3d5691fa-f5dc-4d13-b19c-a169a43aa7b9
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.iwdfiorequest_getreadparameters, IWDFIoRequest::GetReadParameters, UMDFRequestObjectRef_449eedbd-5e32-4e7c-81ee-77a341fa0d75.xml, IWDFIoRequest interface, GetReadParameters method, GetReadParameters method, IWDFIoRequest interface, wudfddi/IWDFIoRequest::GetReadParameters, GetReadParameters method, umdf.iwdfiorequest_getreadparameters, IWDFIoRequest, GetReadParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: wudfddi.h
req.dll: WUDFx.dll
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WUDFx.dll
apiname:
-	IWDFIoRequest.GetReadParameters
product: Windows
targetos: Windows
req.typenames: "*PPOWER_ACTION, POWER_ACTION"
req.product: Windows 10 or later.
---

# IWDFIoRequest::GetReadParameters method


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>GetReadParameters</b> method retrieves the request parameters for a read-type request.


## -syntax


````
void  GetReadParameters(
  [out] SIZE_T   *pSizeInBytes,
  [out] LONGLONG *pllOffset,
  [out] ULONG    *pulKey
);
````


## -parameters




### -param pSizeInBytes [out]

A pointer to a variable that receives the size, in bytes, to read. To retrieve the data for reading, the driver calls the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559112">IWDFIoRequest::GetOutputMemory</a> method.

This parameter is optional. The driver can pass <b>NULL</b> if the driver does not require the information. 


### -param pullOffset




### -param pulKey [out]

A pointer to a variable that receives a key that the driver can use to sort the I/O request in a way that the driver determines.

This parameter is optional. The driver can pass <b>NULL</b> if the driver does not require the information. 


#### - pllOffset [out]

A pointer to a variable that receives the offset, in bytes, to begin reading from the device or the file on the device. If the device does not support absolute read addresses, <i>pllOffset</i> can be ignored. For more information, see the following Remarks section.

Client applications specify this value in the <b>Offset</b> and <b>OffsetHigh</b> members of the OVERLAPPED structure. A pointer to OVERLAPPED is passed in the Microsoft Win32 <b>ReadFile</b> or <b>ReadFileEx</b> function. 

This parameter is optional. The driver can pass <b>NULL</b> if the driver does not require the information. 


## -returns



None




## -remarks



A call to <b>GetReadParameters</b> fails if the request type is not a read type.

For devices that support addressing (for example, a disk device), the value that the <i>pllOffset</i> parameter points to is typically the byte offset into the device. For devices that do not support addressing (for example, a serial port), the driver can ignore the value at <i>pllOffset</i>. 

Although the driver can optionally specify <b>NULL</b> for each of the <i>pSizeInBytes</i>, <i>pllOffset</i>, and <i>pulKey</i> parameters, the driver must specify at least one non-<b>NULL</b> parameter for <b>GetReadParameters</b> to execute successfully.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff559112">IWDFIoRequest::GetOutputMemory</a>



<a href="..\wudfddi\nn-wudfddi-iwdfiorequest.md">IWDFIoRequest</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFIoRequest::GetReadParameters method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

