---
UID: NF:filterpipeline.IXpsDocumentConsumer.SendFixedPage
title: IXpsDocumentConsumer::SendFixedPage method
author: windows-driver-content
description: The SendFixedPage method sends a fixed page of an XPS document to the pipeline.
old-location: print\ixpsdocumentconsumer_sendfixedpage.htm
old-project: print
ms.assetid: ef11161d-5e73-44a8-b802-e3706b78950e
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: SendFixedPage method [Print Devices], filterpipeline_fbf758b4-801f-4c68-879c-2820736e459e.xml, IXpsDocumentConsumer, filterpipeline/IXpsDocumentConsumer::SendFixedPage, SendFixedPage method [Print Devices], IXpsDocumentConsumer interface, SendFixedPage, print.ixpsdocumentconsumer_sendfixedpage, IXpsDocumentConsumer::SendFixedPage, IXpsDocumentConsumer interface [Print Devices], SendFixedPage method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: filterpipeline.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Filterpipeline.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: filterpipeline.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	filterpipeline.h
apiname:
-	IXpsDocumentConsumer.SendFixedPage
product: Windows
targetos: Windows
req.typenames: EXpsFontRestriction
---

# IXpsDocumentConsumer::SendFixedPage method


## -description


The <code>SendFixedPage</code> method sends a fixed page of an XPS document to the pipeline.


## -syntax


````
HRESULT SendFixedPage(
  [in] IFixedPage *pIFixedPage
);
````


## -parameters




### -param pIFixedPage [in]

A pointer to an XPS fixed page object.


## -returns



<code>SendFixedPage</code> returns an <b>HRESULT</b> value.



