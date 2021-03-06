---
UID: NF:printerextension.IPrinterExtensionContextCollection.GetAt
title: IPrinterExtensionContextCollection::GetAt method
author: windows-driver-content
description: Gets a pointer to an IPrinterExtensionContext object.
old-location: print\iprinterextensioncontextcollection_getat.htm
old-project: print
ms.assetid: 5E3DC6C7-E370-4120-81B7-2093812AD009
ms.author: windowsdriverdev
ms.date: 2/2/2018
ms.keywords: GetAt method [Print Devices], GetAt method [Print Devices], IPrinterExtensionContextCollection interface, printerextension/IPrinterExtensionContextCollection::GetAt, IPrinterExtensionContextCollection, IPrinterExtensionContextCollection::GetAt, IPrinterExtensionContextCollection interface [Print Devices], GetAt method, GetAt, print.iprinterextensioncontextcollection_getat, get_GetAt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Desktop
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
-	IPrinterExtensionContextCollection.GetAt
product: Windows
targetos: Windows
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrinterExtensionContextCollection::GetAt method


## -description


Gets a pointer to an <a href="..\printerextension\nn-printerextension-iprinterextensioncontext.md">IPrinterExtensionContext</a> object.


## -syntax


````
HRESULT GetAt(
  [in]          ULONG                    ulIndex,
  [out, retval] IPrinterExtensionContext **ppContext
);
````


## -parameters




### -param ulIndex [in]

The index of the <a href="..\printerextension\nn-printerextension-iprinterextensioncontext.md">IPrinterExtensionContext</a> object within the collection.


### -param ppContext [out, retval]

Pointer to an <a href="..\printerextension\nn-printerextension-iprinterextensioncontext.md">IPrinterExtensionContext</a> interface.


## -returns



This method returns an <b>HRESULT</b> value.




## -see-also

<a href="..\printerextension\nn-printerextension-iprinterextensioncontextcollection.md">IPrinterExtensionContextCollection</a>



<a href="..\printerextension\nn-printerextension-iprinterextensioncontext.md">IPrinterExtensionContext</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrinterExtensionContextCollection::GetAt method%20 RELEASE:%20(2/2/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

