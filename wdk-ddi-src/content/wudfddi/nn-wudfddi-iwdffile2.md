---
UID: NN:wudfddi.IWDFFile2
title: IWDFFile2
author: windows-driver-content
description: Drivers obtain the IWDFFile2 interface by calling IWDFFile::QueryInterface.
old-location: wdf\iwdffile2.htm
old-project: wdf
ms.assetid: 49a3defc-d86c-4d70-8c1c-a5abbadda013
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.iwdffile2, IWDFFile2 interface, IWDFFile2 interface, described, IWDFFile2, wudfddi/IWDFFile2, UMDFFileObjectRef_991af5dd-c654-4afe-9072-0efeb7ab4d57.xml, umdf.iwdffile2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wudfddi.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.9
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
-	IWDFFile2
product: Windows
targetos: Windows
req.typenames: "*PPOWER_ACTION, POWER_ACTION"
req.product: Windows 10 or later.
---

# IWDFFile2 interface


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

Drivers obtain the <b>IWDFFile2</b> interface by calling <b>IWDFFile::QueryInterface</b>.


## -members

The <b>IWDFFile2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff558917">IWDFFile2::GetRelatedFileObject</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0ac5c19a-b3ec-4f1e-a018-2c11cc18e58d">GetRelatedFileObject</a> method retrieves the <a href="..\wudfddi\nn-wudfddi-iwdffile.md">IWDFFile</a> interface of a <i>related file object</i>, which is a file object that has a technology-specific relationship with another file object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff558920">IWDFFile2::RetrieveCountedFileName</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0b3aa8d9-1947-4e5e-91d1-6f73ddb3908a">RetrieveCountedFileName</a> method retrieves the full counted file name for a file that is associated with a device. 

</td>
</tr>
</table>The <a href="https://msdn.microsoft.com/0ac5c19a-b3ec-4f1e-a018-2c11cc18e58d">GetRelatedFileObject</a> method retrieves the <a href="..\wudfddi\nn-wudfddi-iwdffile.md">IWDFFile</a> interface of a <i>related file object</i>, which is a file object that has a technology-specific relationship with another file object.

The <a href="https://msdn.microsoft.com/0b3aa8d9-1947-4e5e-91d1-6f73ddb3908a">RetrieveCountedFileName</a> method retrieves the full counted file name for a file that is associated with a device. 

 

