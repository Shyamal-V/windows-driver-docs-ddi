---
UID: NF:printerextension.IPrintSchemaPageImageableSize.get_OriginWidthInMicrons
title: IPrintSchemaPageImageableSize::get_OriginWidthInMicrons method
author: windows-driver-content
description: Gets the horizontal origin of the imageable area relative to the application media size.
old-location: print\iprintschemapageimageablesize_originwidthinmicrons.htm
old-project: print
ms.assetid: 158F8979-682B-4836-9EC5-6F30371DB6EA
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: OriginWidthInMicrons property [Print Devices], IPrintSchemaPageImageableSize interface, OriginWidthInMicrons property [Print Devices], IPrintSchemaPageImageableSize.OriginWidthInMicrons, printerextension/IPrintSchemaPageImageableSize::OriginWidthInMicrons, IPrintSchemaPageImageableSize::get_OriginWidthInMicrons, printerextension/IPrintSchemaPageImageableSize::get_OriginWidthInMicrons, IPrintSchemaPageImageableSize interface [Print Devices], OriginWidthInMicrons property, IPrintSchemaPageImageableSize, print.iprintschemapageimageablesize_originwidthinmicrons, get_OriginWidthInMicrons
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: printerextension.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	Printerextension.h
apiname:
-	IPrintSchemaPageImageableSize.OriginWidthInMicrons
-	IPrintSchemaPageImageableSize.get_OriginWidthInMicrons
product: Windows
targetos: Windows
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrintSchemaPageImageableSize::get_OriginWidthInMicrons method


## -description


Gets the horizontal origin of the imageable area relative to the application media size.

This property is read-only.


## -syntax


````
HRESULT get_OriginWidthInMicrons(
  [out, retval] ULONG *pulOriginWidth
);
````


## -parameters


## -see-also

<a href="..\printerextension\nn-printerextension-iprintschemapageimageablesize.md">IPrintSchemaPageImageableSize</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrintSchemaPageImageableSize::OriginWidthInMicrons property%20 RELEASE:%20(2/2/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

