---
UID: NF:wdtfdriverpackageaction.IWDTFDriverPackageAction2.get_CatalogFile
title: IWDTFDriverPackageAction2::get_CatalogFile method
author: windows-driver-content
description: Gets the catalog file name.
old-location: dtf\iwdtfdriverpackageaction2_catalogfile.htm
old-project: dtf
ms.assetid: 57cfb693-7134-4e3c-a5b4-3d15456b4daa
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: Microsoft::WDTF::IWDTFDriverPackageAction2::CatalogFile, get_CatalogFile, CatalogFile property [Windows Device Testing Framework], CatalogFile property [Windows Device Testing Framework], IWDTFDriverPackageAction2 interface, IWDTFDriverPackageAction2.CatalogFile, wdtfdriverpackageaction/IWDTFDriverPackageAction2::get_CatalogFile, IWDTFDriverPackageAction2, IWDTFDriverPackageAction2::get_CatalogFile, IWDTFDriverPackageAction2 interface [Windows Device Testing Framework], CatalogFile property, dtf.iwdtfdriverpackageaction2_catalogfile, Microsoft.WDTF.IWDTFDriverPackageAction2.CatalogFile, wdtfdriverpackageaction/IWDTFDriverPackageAction2::CatalogFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfdriverpackageaction.h
req.include-header: 
req.target-type: Windows
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
-	IWDTFDriverPackageAction2.CatalogFile
-	IWDTFDriverPackageAction2.get_CatalogFile
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFDriverPackageAction2::get_CatalogFile method


## -description


Gets the catalog file name.

This property is read-only.


## -syntax


````
HRESULT get_CatalogFile(
  [out, retval] BSTR *pVal
);
````


## -parameters


## -see-also

<a href="..\wdtfdriverpackageaction\nn-wdtfdriverpackageaction-iwdtfdriverpackageaction2.md">IWDTFDriverPackageAction2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFDriverPackageAction2::CatalogFile property%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

