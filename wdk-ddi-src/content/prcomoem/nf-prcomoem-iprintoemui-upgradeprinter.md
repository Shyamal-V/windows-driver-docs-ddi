---
UID: NF:prcomoem.IPrintOemUI.UpgradePrinter
title: IPrintOemUI::UpgradePrinter method
author: windows-driver-content
description: The IPrintOemUI::UpgradePrinter method allows a user interface plug-in to upgrade device option values that are stored in the registry.
old-location: print\iprintoemui_upgradeprinter.htm
old-project: print
ms.assetid: 405f0000-c239-4f2c-83ad-5d35441a5df2
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: print.iprintoemui_upgradeprinter, print_unidrv-pscript_ui_18087d8a-d7b4-485f-84fb-277e194bb4e8.xml, UpgradePrinter method [Print Devices], IPrintOemUI interface [Print Devices], UpgradePrinter method, prcomoem/IPrintOemUI::UpgradePrinter, IPrintOemUI::UpgradePrinter, IPrintOemUI, UpgradePrinter method [Print Devices], IPrintOemUI interface, UpgradePrinter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: prcomoem.h
req.include-header: Prcomoem.h
req.target-type: Desktop
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
req.lib: prcomoem.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	prcomoem.h
apiname:
-	IPrintOemUI.UpgradePrinter
product: Windows
targetos: Windows
req.typenames: OEMPTOPTS, *POEMPTOPTS
req.product: Windows 10 or later.
---

# IPrintOemUI::UpgradePrinter method


## -description


The <code>IPrintOemUI::UpgradePrinter</code> method allows a user interface plug-in to upgrade device option values that are stored in the registry.


## -syntax


````
HRESULT UpgradePrinter(
   DWORD dwLevel,
   PBYTE pDriverUpgradeInfo
);
````


## -parameters




### -param dwLevel

Caller-supplied version number of the structure pointed to by <i>pDriverUpgradeInfo</i>. Current valid value is 1.


### -param pDriverUpgradeInfo

Caller-supplied pointer to a <a href="..\winddiui\ns-winddiui-_driver_upgrade_info_1.md">DRIVER_UPGRADE_INFO_1</a> structure.


## -returns



The method must return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>
 




## -remarks



If you provide a user interface plug-in for one of Microsoft's printer drivers, and if the user interface plug-in stores device option values in the registry, it should implement the <code>IPrintOemUI::UpgradePrinter</code> method to update those values.

A user interface plug-in's <code>IPrintOemUI::UpgradePrinter</code> method performs the same types of operations as the <b>DrvUpgradePrinter</b> function that is exported by user-mode printer interface DLLs. When the driver's <a href="..\winddiui\nf-winddiui-drvupgradeprinter.md">DrvUpgradePrinter</a> function is called, it updates its own registry values and then calls the <code>IPrintOemUI::UpgradePrinter</code> method.

If <code>IPrintOemUI::UpgradePrinter</code> methods are exported by multiple user interface plug-ins, the methods are called in the order that the plug-ins are specified for installation.

For more information about creating and installing user interface plug-ins, see <a href="https://msdn.microsoft.com/b7761209-1f6f-4288-af47-4ed855c2e629">Customizing Microsoft's Printer Drivers</a>.



