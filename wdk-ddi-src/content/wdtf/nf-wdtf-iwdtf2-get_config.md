---
UID: NF:wdtf.IWDTF2.get_Config
title: IWDTF2::get_Config method
author: windows-driver-content
description: Gets the WDTF configuration object.
old-location: dtf\iwdtf2_config.htm
old-project: dtf
ms.assetid: d7302c51-02b3-4876-b215-6bde1160245a
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IWDTF2::get_Config, Microsoft::WDTF::IWDTF2::Config, dtf.iwdtf2_config, get_Config, Config property [Windows Device Testing Framework], IWDTF2 interface, wdtf/IWDTF2::Config, wdtf/IWDTF2::get_Config, Microsoft.WDTF.IWDTF2.Config, IWDTF2, IWDTF2 interface [Windows Device Testing Framework], Config property, IWDTF2.Config, Config property [Windows Device Testing Framework]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtf.h
req.include-header: 
req.target-type: Windows
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
-	IWDTF2.Config
-	IWDTF2.get_Config
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTF2::get_Config method


## -description


Gets the WDTF configuration object.

This property is read-only.


## -syntax


````
HRESULT get_Config(
  [out, retval] IWDTFCONFIG2 **ppConfig
);
````


## -parameters


## -see-also

<a href="..\wdtf\nn-wdtf-iwdtfconfig2.md">IWDTFConfig2</a>



<a href="..\wdtf\nn-wdtf-iwdtf2.md">IWDTF2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTF2::Config property%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

