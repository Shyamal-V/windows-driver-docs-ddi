---
UID: NF:wdtf.IWDTFTargets2.Remove
title: IWDTFTargets2::Remove method
author: windows-driver-content
description: Removes an item from the collection.
old-location: dtf\iwdtftargets2_remove.htm
old-project: dtf
ms.assetid: 5db8c912-a446-4ae7-a775-f56ffa979283
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: Remove method [Windows Device Testing Framework], IWDTFTargets2 interface, Microsoft::WDTF::IWDTFTargets2::Remove, wdtf/IWDTFTargets2::Remove, IWDTFTargets2::Remove, Remove method [Windows Device Testing Framework], Remove, dtf.iwdtftargets2_remove, IWDTFTargets2 interface [Windows Device Testing Framework], Remove method, Microsoft.WDTF.IWDTFTargets2.Remove, IWDTFTargets2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtf.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTF.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTF.Interop.metadata_dll
req.type-library: 
req.lib: wdtf.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTF.Interop.metadata_dll.dll
apiname:
-	IWDTFTargets2.Remove
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFTargets2::Remove method


## -description


Removes an item from the collection.


## -syntax


````
HRESULT Remove(
  [in] IWDTFTarget2 *pTarget
);
````


## -parameters




### -param pTarget [in]

The item to remove from this collection.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The lifetime of <a href="..\wdtf\nn-wdtf-iwdtftarget2.md">IWDTFTarget2</a> interface 
instances are tied to their creator. If you remove an item from a collection, the item is
not destroyed.




## -see-also

<a href="..\wdtf\nn-wdtf-iwdtftargets2.md">IWDTFTargets2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFTargets2::Remove method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

