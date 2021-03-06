---
UID: NF:prcomoem.IPrintOemPS.PublishDriverInterface
title: IPrintOemPS::PublishDriverInterface method
author: windows-driver-content
description: The IPrintOemPS::PublishDriverInterface method allows a rendering plug-in for Pscript5 to obtain the Pscript5 driver's IPrintCorePS2, IPrintOemDriverPS, or IPrintCoreHelperPS interface.
old-location: print\iprintoemps_publishdriverinterface.htm
old-project: print
ms.assetid: f878a674-7c08-4a7a-ab00-6c79f02566be
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: PublishDriverInterface method [Print Devices], PublishDriverInterface method [Print Devices], IPrintOemPS interface, IPrintOemPS::PublishDriverInterface, PublishDriverInterface, IPrintOemPS interface [Print Devices], PublishDriverInterface method, prcomoem/IPrintOemPS::PublishDriverInterface, IPrintOemPS, print_unidrv-pscript_rendering_b7e2dc4b-ecc1-41bd-853d-4099614b5cae.xml, print.iprintoemps_publishdriverinterface
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
-	IPrintOemPS.PublishDriverInterface
product: Windows
targetos: Windows
req.typenames: OEMPTOPTS, *POEMPTOPTS
req.product: Windows 10 or later.
---

# IPrintOemPS::PublishDriverInterface method


## -description


The <code>IPrintOemPS::PublishDriverInterface</code> method allows a rendering plug-in for Pscript5 to obtain the Pscript5 driver's <b>IPrintCorePS2</b>, <b>IPrintOemDriverPS</b>, or <b>IPrintCoreHelperPS</b> interface.


## -syntax


````
HRESULT PublishDriverInterface(
   IUnknown *pIUnknown
);
````


## -parameters




### -param pIUnknown

Caller-supplied pointer to the <b>IUnknown</b> interface of the driver's <a href="https://msdn.microsoft.com/d5eb6962-2201-405f-9a22-2b11fb6d0360">IPrintCorePS2 COM Interface</a>, <a href="https://msdn.microsoft.com/32975728-501f-45ac-a53d-34cf286bc433">IPrintOemDriverPS COM Interface</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/ff552906">IPrintCoreHelperPS Interface</a>.


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
The operation failed

</td>
</tr>
</table>
 




## -remarks



The Pscript5 driver supports the <b>IPrintCorePS2</b>, <b>IPrintOemDriverPS</b>, and <b>IPrintCoreHelperPS</b> interfaces. A rendering plug-in for Pscript5 must implement the <code>IPrintOemPS::PublishDriverInterface</code> method. The method should return information on its supported Pscript5 interfaces as follows:

<ol>
<li>
The Pscript5 driver first calls the <code>IPrintOemPS::PublishDriverInterface</code> method with the <i>pIUnknown</i> pointer set to the <b>IPrintCorePS2</b> instance's <b>IUnknown</b> interface. If the rendering plug-in is able to use the <b>IPrintCorePS2</b> interface, the method must return S_OK. Otherwise, the plug-in should return E_FAIL.

</li>
<li>
If the plug-in has returned E_FAIL, the Pscript5 driver calls the <code>IPrintOemPS::PublishDriverInterface</code> method again, but with the <i>pIUnknown</i> pointer set to the <b>IPrintOemDriverPS</b> instance's <b>IUnknown</b> interface. If the plug-in is able to use the <b>IPrintOemDriverPS</b> interface, the method must return S_OK. Otherwise, the plug-in should return E_FAIL.

</li>
<li>
If the plug-in's <a href="https://msdn.microsoft.com/library/windows/hardware/ff553221">IPrintOemPS::GetInfo</a> method has returned a value of OEMPUBLISH_IPRINTCOREHELPER in <i>pBuffer</i> in response to a call with <i>dwMode</i> set to OEMGI_GETREQUESTEDHELPERINTERFACES in <i>pBuffer</i>, the Pscript5 driver calls the <code>IPrintOemPS::PublishDriverInterface</code> method again, but with the <i>pIUnknown</i> pointer set to an object that implements the <b>IPrintCoreHelperPS</b> and <b>IPrintCoreHelper</b> interfaces. If the plug-in retains a pointer to the object interface, the method should return S_OK. Otherwise, the method should return E_FAIL.

</li>
</ol>
If the plug-in fails all calls to <code>IPrintOemPS::PublishDriverInterface</code>, the plug-in will not receive further calls. If the plug-in will be calling <b>IPrintCorePS2</b>, <b>IPrintOemDriverPS</b>, or <b>IPrintCoreHelperPS</b> interface methods, it must use the received <b>IUnknown</b> interface pointer to call <b>IUnknown::QueryInterface</b> (described in the Microsoft Windows SDK documentation) in order to obtain a pointer to the driver's supported version of the <b>IPrintCorePS2</b>, <b>IPrintOemDriverPS</b>, or <b>IPrintCoreHelperPS</b> interface. For more information, see <a href="https://msdn.microsoft.com/021ba789-99bd-4ab5-98fb-0d24ffd0ce25">Accessing Printer Driver Interfaces from Plug-Ins</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff553221">IPrintOemPS::GetInfo</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrintOemPS::PublishDriverInterface method%20 RELEASE:%20(2/2/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

