---
UID: NN:wdtfdriversetupdeviceaction.IWDTFDriverSetupAction2
title: IWDTFDriverSetupAction2
author: windows-driver-content
description: Defines operations that control the target device during driver setup.
old-location: dtf\iwdtfdriversetupaction2.htm
old-project: dtf
ms.assetid: 474590f9-f737-4b9a-9a63-8cce8a35c538
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: dtf.iwdtfdriversetupaction2, IWDTFDriverSetupAction2 interface [Windows Device Testing Framework], IWDTFDriverSetupAction2 interface [Windows Device Testing Framework], described, IWDTFDriverSetupAction2, wdtfdriversetupdeviceaction/IWDTFDriverSetupAction2, Microsoft.WDTF.IWDTFDriverSetupAction2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wdtfdriversetupdeviceaction.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFDriverSetupDeviceAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverSetupDeviceAction.Interop.dll
req.type-library: 
req.lib: wdtfdriversetupdeviceaction.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTFDriverSetupDeviceAction.Interop.dll
apiname:
-	IWDTFDriverSetupAction2
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFDriverSetupAction2 interface


## -description


Defines operations that control the target device during driver setup.


## -members

The <b>IWDTFDriverSetupAction2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450941">UnInstallDriverPermanently</a>
</td>
<td align="left" width="63%">
Uninstalls the current driver for the target device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450945">UpdateDriver</a>
</td>
<td align="left" width="63%">
Updates the target device with a driver from the driver package.

</td>
</tr>
</table>Uninstalls the current driver for the target device.

Updates the target device with a driver from the driver package.

 

