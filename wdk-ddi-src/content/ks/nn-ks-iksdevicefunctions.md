---
UID: NN:ks.IKsDeviceFunctions
title: IKsDeviceFunctions
author: windows-driver-content
description: The IKsDeviceFunctions interface is a COM-style interface implemented on AVStream devices. This interface is available in Windows Server 2003 SP1 and later versions of Windows.
old-location: stream\iksdevicefunctions.htm
old-project: stream
ms.assetid: d29e7b39-5fcf-4543-9363-6f8ac6a9c7dc
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: stream.iksdevicefunctions, IKsDeviceFunctions interface [Streaming Media Devices], IKsDeviceFunctions interface [Streaming Media Devices], described, IKsDeviceFunctions, ks/IKsDeviceFunctions, avintfc_68e124c6-7a91-4c68-8327-e2c83b982699.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ks.h
req.include-header: 
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
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	ks.h
apiname:
-	IKsDeviceFunctions
product: Windows
targetos: Windows
req.typenames: 
---

# IKsDeviceFunctions interface


## -description


The IKsDeviceFunctions interface is a COM-style interface implemented on AVStream devices. This interface is available in Windows Server 2003 SP1 and later versions of Windows.


## -members

The <b>IKsDeviceFunctions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5dc54a6-e26a-455b-9990-92f5cfece923">RegisterAdapterObjectEx</a>
</td>
<td align="left" width="63%">
Registers a DMA adapter object with AVStream. All drivers compiled for Win64 should use this method instead of <a href="..\ks\nf-ks-ksdeviceregisteradapterobject.md">KsDeviceRegisterAdapterObject</a>.

</td>
</tr>
</table>Registers a DMA adapter object with AVStream. All drivers compiled for Win64 should use this method instead of <a href="..\ks\nf-ks-ksdeviceregisteradapterobject.md">KsDeviceRegisterAdapterObject</a>.

 

