---
UID: NF:wdtf.IWDTFTarget2.Eval
title: IWDTFTarget2::Eval method
author: windows-driver-content
description: Evaluate whether this target matches an SDEL statement.
old-location: dtf\iwdtftarget2_eval.htm
old-project: dtf
ms.assetid: 468cb35d-f816-4233-ba07-8dc47b77d442
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: Microsoft::WDTF::IWDTFTarget2::Eval, IWDTFTarget2 interface [Windows Device Testing Framework], Eval method, dtf.iwdtftarget2_eval, IWDTFTarget2, Eval method [Windows Device Testing Framework], IWDTFTarget2 interface, Microsoft.WDTF.IWDTFTarget2.Eval, wdtf/IWDTFTarget2::Eval, IWDTFTarget2::Eval, Eval, Eval method [Windows Device Testing Framework]
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
-	IWDTFTarget2.Eval
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFTarget2::Eval method


## -description


Evaluate whether this target matches an SDEL statement.


## -syntax


````
HRESULT Eval(
  [in]          BSTR         SDEL,
  [out, retval] VARIANT_BOOL *pResult
);
````


## -parameters




### -param SDEL [in]

The SDEL statement.


### -param pResult [out, retval]

True if the SDEL statement matches this target; 
otherwise, alse.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\wdtf\nn-wdtf-iwdtftarget2.md">IWDTFTarget2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFTarget2::Eval method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

