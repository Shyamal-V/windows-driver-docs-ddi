---
UID: NN:wudfddi.IRemoteInterfaceCallbackRemoval
title: IRemoteInterfaceCallbackRemoval
author: windows-driver-content
description: The IRemoteInterfaceCallbackRemoval provides a callback function that the framework calls to notify the driver about the removal of a device interface.
old-location: wdf\iremoteinterfacecallbackremoval.htm
old-project: wdf
ms.assetid: f4cbad57-922f-4265-b436-847feeca853c
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.iremoteinterfacecallbackremoval, IRemoteInterfaceCallbackRemoval interface, IRemoteInterfaceCallbackRemoval interface, described, IRemoteInterfaceCallbackRemoval, wudfddi/IRemoteInterfaceCallbackRemoval, UMDFIoTargetObjectRef_7eeb5a11-5f99-4b2c-a36f-0fd72466e278.xml, umdf.iremoteinterfacecallbackremoval
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wudfddi.h
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
req.lib: wudfddi.h
req.dll: WUDFx.dll
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	wudfddi.h
apiname:
-	IRemoteInterfaceCallbackRemoval
product: Windows
targetos: Windows
req.typenames: "*PPOWER_ACTION, POWER_ACTION"
req.product: Windows 10 or later.
---

# IRemoteInterfaceCallbackRemoval interface


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>IRemoteInterfaceCallbackRemoval</b> provides a callback function that the framework calls to notify the driver about the removal of a <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-device-interfaces-in-umdf-drivers">device interface</a>.


## -members

The <b>IRemoteInterfaceCallbackRemoval</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556893">IRemoteInterfaceCallbackRemoval::OnRemoteInterfaceRemoval</a>
</td>
<td align="left" width="63%">
A UMDF-based driver's <a href="https://msdn.microsoft.com/0dfa2eb8-a7f6-46d9-9599-5e2aaf583f78">OnRemoteInterfaceRemoval</a> event callback function notifies the driver that it cannot use a <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-device-interfaces-in-umdf-drivers">device interface</a> because the interface has been removed.

</td>
</tr>
</table>A UMDF-based driver's <a href="https://msdn.microsoft.com/0dfa2eb8-a7f6-46d9-9599-5e2aaf583f78">OnRemoteInterfaceRemoval</a> event callback function notifies the driver that it cannot use a <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-device-interfaces-in-umdf-drivers">device interface</a> because the interface has been removed.

 


## -remarks



If your driver supports an <b>IRemoteInterfaceCallbackRemoval</b> interface for a device, the <b>IUnknown::QueryInterface</b> method that the driver passes to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556925">IWDFDevice2::CreateRemoteInterface</a> must return the interface. 



