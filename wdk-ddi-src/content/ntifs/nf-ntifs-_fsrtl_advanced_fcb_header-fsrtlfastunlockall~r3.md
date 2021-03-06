---
UID: NF:ntifs._FSRTL_ADVANCED_FCB_HEADER.FsRtlFastUnlockAll~r3
title: FsRtlFastUnlockAll function
author: windows-driver-content
description: The FsRtlFastUnlockAll routine releases all byte-range locks that were acquired by the specified process for a file.
old-location: ifsk\fsrtlfastunlockall.htm
old-project: ifsk
ms.assetid: 5004fb3c-f2e3-4663-9b95-7fb7bb38364d
ms.author: windowsdriverdev
ms.date: 2/7/2018
ms.keywords: FsRtlFastUnlockAll, ntifs/FsRtlFastUnlockAll, ifsk.fsrtlfastunlockall, fsrtlref_713fc415-f52e-4e0f-8806-02f44fb9b3f4.xml, FsRtlFastUnlockAll routine [Installable File System Drivers]
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
req.irql: "<= APC_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	DllExport
apilocation:
-	NtosKrnl.exe
apiname:
-	FsRtlFastUnlockAll
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# FsRtlFastUnlockAll function


## -description


The <b>FsRtlFastUnlockAll</b> routine releases all byte-range locks that were acquired by the specified process for a file. 


## -syntax


````
NTSTATUS FsRtlFastUnlockAll(
  _In_     PFILE_LOCK   FileLock,
  _In_     PFILE_OBJECT FileObject,
  _In_     PEPROCESS    ProcessId,
  _In_opt_ PVOID        Context
);
````


## -parameters




### -param FileLock [in]

Pointer to the FILE_LOCK structure for the file. This structure must have been initialized by a previous call to <a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlallocatefilelock~r1.md">FsRtlAllocateFileLock</a> or <a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlinitializefilelock~r2.md">FsRtlInitializeFileLock</a>.


### -param FileObject [in]

Pointer to the file object for the file.


### -param ProcessId [in]

Pointer to the process ID for the process.


### -param Context [in, optional]

Optional context pointer to be used when completing IRPs. 


## -returns



<b>FsRtlFastUnlockAll</b> returns STATUS_SUCCESS or an error status code such as STATUS_RANGE_NOT_LOCKED. 




## -remarks



After releasing the byte-range locks, <b>FsRtlFastUnlockAll</b> completes any currently queued lock IRPs that can now be completed.




## -see-also

<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlinitializefilelock~r2.md">FsRtlInitializeFileLock</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlallocatefilelock~r1.md">FsRtlAllocateFileLock</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FsRtlFastUnlockAll routine%20 RELEASE:%20(2/7/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

