---
UID: NF:wdtfdriverpackageaction.IWDTFDriverPackageAction2.Compare
title: IWDTFDriverPackageAction2::Compare method
author: windows-driver-content
description: Compares two driver packages.
old-location: dtf\iwdtfdriverpackageaction2_compare.htm
old-project: dtf
ms.assetid: fa93d535-fe26-40cc-b08a-88841dcfdc96
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: dtf.iwdtfdriverpackageaction2_compare, IWDTFDriverPackageAction2 interface [Windows Device Testing Framework], Compare method, Compare, Compare method [Windows Device Testing Framework], IWDTFDriverPackageAction2 interface, IWDTFDriverPackageAction2::Compare, IWDTFDriverPackageAction2, Compare method [Windows Device Testing Framework], Microsoft::WDTF::IWDTFDriverPackageAction2::Compare, Microsoft.WDTF.IWDTFDriverPackageAction2.Compare, wdtfdriverpackageaction/IWDTFDriverPackageAction2::Compare
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfdriverpackageaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFDriverPackageAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverPackageAction.Interop.dll
req.type-library: 
req.lib: wdtfdriverpackageaction.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTFDriverPackageAction.Interop.dll
apiname:
-	IWDTFDriverPackageAction2.Compare
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFDriverPackageAction2::Compare method


## -description


Compares two driver packages.


## -syntax


````
HRESULT Compare(
  [in]          IWDTFDriverPackageAction2 *pDp,
  [out, retval] VARIANT_BOOL              *pbIsIdentical
);
````


## -parameters




### -param pDp [in]

The second driver package.


### -param pbIsIdentical [out, retval]

True if the two driver packages are the same; 
otherwise, false.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\wdtfdriverpackageaction\nn-wdtfdriverpackageaction-iwdtfdriverpackageaction2.md">IWDTFDriverPackageAction2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFDriverPackageAction2::Compare method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

