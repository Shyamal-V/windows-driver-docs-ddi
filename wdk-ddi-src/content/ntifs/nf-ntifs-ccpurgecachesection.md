---
UID: NF:ntifs.CcPurgeCacheSection
title: CcPurgeCacheSection function
author: windows-driver-content
description: The CcPurgeCacheSection routine purges all or a portion of a cached file from the system cache.
old-location: ifsk\ccpurgecachesection.htm
old-project: ifsk
ms.assetid: 7f9cff3b-0780-4fc4-8b1a-b0af0506712a
ms.author: windowsdriverdev
ms.date: 2/7/2018
ms.keywords: CcPurgeCacheSection, ifsk.ccpurgecachesection, ccref_587b0f92-f80a-42f2-b3bb-dae27208b796.xml, ntifs/CcPurgeCacheSection, CcPurgeCacheSection routine [Installable File System Drivers]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: "< DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	DllExport
apilocation:
-	NtosKrnl.exe
apiname:
-	CcPurgeCacheSection
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# CcPurgeCacheSection function


## -description


The <b>CcPurgeCacheSection</b> routine purges all or a portion of a cached file from the system cache.


## -syntax


````
BOOLEAN CcPurgeCacheSection(
  _In_     PSECTION_OBJECT_POINTERS SectionObjectPointer,
  _In_opt_ PLARGE_INTEGER           FileOffset,
  _In_     ULONG                    Length,
  _In_     ULONG                    UninitializeCacheMaps
);
````


## -parameters




### -param SectionObjectPointer [in]

Pointer to a structure containing the file object's section object pointers.


### -param FileOffset [in, optional]

Pointer to a variable that specifies the starting byte offset within the cached file where the data is to be purged. 

If <i>FileOffset</i> is <b>NULL</b>, the entire file is purged from the cache.

If <i>FileOffset</i> is not <b>NULL</b>, only the byte range specified by <i>FileOffset</i> and <i>Length</i> is purged.


### -param Length [in]

Length of the byte range to purge, starting at <i>FileOffset</i>. If <i>Length</i> is zero, the range from <i>FileOffset</i> to the end of the file is purged. If <i>FileOffset</i> is <b>NULL</b>, <i>Length</i> is ignored.


### -param Flags

TBD




#### - UninitializeCacheMaps [in]

Set to <b>TRUE</b> to uninitialize any private cache maps for the file before purging the file data.


## -returns



<b>CcPurgeCacheSection</b> returns <b>TRUE</b> if the cached file data was successfully purged, <b>FALSE</b> otherwise.




## -remarks



File systems call <b>CcPurgeCacheSection</b> to purge stale data from the cache. For example, when a file is truncated but not deleted, <b>CcPurgeCacheSection</b> should be called to purge any cached data that is no longer part of the file.

<b>CcPurgeCacheSection</b> will not purge mapped files. 

Before calling <b>CcPurgeCacheSection</b>, the caller must acquire the file exclusively and ensure that no thread, including the caller, has mapped or pinned any byte range in the file. 




## -see-also

<a href="..\ntifs\nf-ntifs-ccflushcache.md">CcFlushCache</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539143">CcIsFileCached</a>



<a href="..\ntifs\nf-ntifs-ccuninitializecachemap.md">CcUninitializeCacheMap</a>



<a href="..\ntifs\nf-ntifs-ccinitializecachemap.md">CcInitializeCacheMap</a>



<a href="..\ntifs\nf-ntifs-mmflushimagesection.md">MmFlushImageSection</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20CcPurgeCacheSection routine%20 RELEASE:%20(2/7/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

