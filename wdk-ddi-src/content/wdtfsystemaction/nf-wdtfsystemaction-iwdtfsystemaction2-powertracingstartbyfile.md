---
UID: NF:wdtfsystemaction.IWDTFSystemAction2.PowerTracingStartByFile
title: IWDTFSystemAction2::PowerTracingStartByFile method
author: windows-driver-content
description: Starts a trace session for power state transitions and saves the trace message file (.etl) using the specified path. This method is available starting with Windows 8.
old-location: dtf\iwdtfsystemaction2_powertracingstartbyfile.htm
old-project: dtf
ms.assetid: c37095d2-fbf5-49fa-a6c8-b4776bf530af
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: wdtfsystemaction/IWDTFSystemAction2::PowerTracingStartByFile, Microsoft::WDTF::IWDTFSystemAction2::PowerTracingStartByFile, IWDTFSystemAction2, IWDTFSystemAction2::PowerTracingStartByFile, IWDTFSystemAction2 interface [Windows Device Testing Framework], PowerTracingStartByFile method, PowerTracingStartByFile method [Windows Device Testing Framework], Microsoft.WDTF.IWDTFSystemAction2.PowerTracingStartByFile, PowerTracingStartByFile, PowerTracingStartByFile method [Windows Device Testing Framework], IWDTFSystemAction2 interface, dtf.iwdtfsystemaction2_powertracingstartbyfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfsystemaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFSystemAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFSystemAction.Interop.dll
req.type-library: 
req.lib: wdtfsystemaction.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	WDTFSystemAction.Interop.dll
apiname:
-	IWDTFSystemAction2.PowerTracingStartByFile
product: Windows
targetos: Windows
req.typenames: "*PWORK_QUEUE_ITEM, WORK_QUEUE_ITEM"
req.product: Windows 10 or later.
---

# IWDTFSystemAction2::PowerTracingStartByFile method


## -description


Starts a trace session for power state transitions and saves the trace message file (.etl) using the specified path. This method is available starting with Windows 8.



## -syntax


````
HRESULT PowerTracingStartByFile(
  [in] BSTR EventFilePath
);
````


## -parameters




### -param EventFilePath [in]

Specifies the location to store the trace message (.etl)
    log file.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\wdtfsystemaction\nn-wdtfsystemaction-iwdtfsystemaction2.md">IWDTFSystemAction2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [dtf\dtf]:%20IWDTFSystemAction2::PowerTracingStartByFile method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

