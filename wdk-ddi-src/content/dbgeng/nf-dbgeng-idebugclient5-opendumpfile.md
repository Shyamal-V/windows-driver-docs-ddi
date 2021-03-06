---
UID: NF:dbgeng.IDebugClient5.OpenDumpFile
title: IDebugClient5::OpenDumpFile method
author: windows-driver-content
description: The OpenDumpFile method opens a dump file as a debugger target.
old-location: debugger\opendumpfile.htm
old-project: debugger
ms.assetid: c04b79a0-ef20-4ba5-aba9-9335b095cfef
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: OpenDumpFile method [Windows Debugging], IDebugClient4 interface, IDebugClient_4ab673e2-629c-455a-8d40-27465005375f.xml, IDebugClient5, IDebugClient3, IDebugClient3::OpenDumpFile, IDebugClient interface [Windows Debugging], OpenDumpFile method, dbgeng/IDebugClient2::OpenDumpFile, IDebugClient, IDebugClient2 interface [Windows Debugging], OpenDumpFile method, OpenDumpFile method [Windows Debugging], OpenDumpFile method [Windows Debugging], IDebugClient5 interface, OpenDumpFile, OpenDumpFile method [Windows Debugging], IDebugClient3 interface, debugger.opendumpfile, IDebugClient5 interface [Windows Debugging], OpenDumpFile method, IDebugClient4::OpenDumpFile, IDebugClient2, dbgeng/IDebugClient4::OpenDumpFile, IDebugClient2::OpenDumpFile, IDebugClient::OpenDumpFile, IDebugClient4 interface [Windows Debugging], OpenDumpFile method, OpenDumpFile method [Windows Debugging], IDebugClient interface, dbgeng/IDebugClient5::OpenDumpFile, IDebugClient4, dbgeng/IDebugClient::OpenDumpFile, IDebugClient3 interface [Windows Debugging], OpenDumpFile method, dbgeng/IDebugClient3::OpenDumpFile, OpenDumpFile method [Windows Debugging], IDebugClient2 interface, IDebugClient5::OpenDumpFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
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
req.lib: dbgeng.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	dbgeng.h
apiname:
-	IDebugClient.OpenDumpFile
-	IDebugClient2.OpenDumpFile
-	IDebugClient3.OpenDumpFile
-	IDebugClient4.OpenDumpFile
-	IDebugClient5.OpenDumpFile
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugClient5::OpenDumpFile method


## -description


The <b>OpenDumpFile</b> method opens a dump file as a debugger target.


## -syntax


````
HRESULT OpenDumpFile(
  [in] PCSTR DumpFile
);
````


## -parameters




### -param DumpFile [in]

Specifies the name of the dump file to open.  <i>DumpFile</i> must include the file name extension. <i>DumpFile</i> can include a relative or absolute path; relative paths are relative to the directory in which the debugger was started.  <i>DumpFile</i> can have the form of a file URL, starting with "file://".  If <i>DumpFile</i> specifies a cabinet (.cab) file, the cabinet file is searched for the first file with extension .kdmp, then .hdmp, then .mdmp, and finally .dmp.


## -returns



This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -remarks



The Unicode version of this method is <a href="https://msdn.microsoft.com/library/windows/hardware/ff552324">OpenDumpFileWide</a>.

<div class="alert"><b>Note</b>    The engine doesn't completely attach to the dump file until the <a href="https://msdn.microsoft.com/library/windows/hardware/ff561229">WaitForEvent</a> method has been called.  When a dump file is created from a process or kernel, information about the last event is stored in the dump file.  After the dump file is opened, the next time execution is attempted, the engine will generate this event for the event callbacks.  Only then does the dump file become available in the debugging session.</div>
<div> </div>
For more information about crash dump files, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff542783">Dump-File Targets</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff552324">OpenDumpFileWide</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient.md">IDebugClient</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient3.md">IDebugClient3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537874">AddDumpInformationFileWide</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537865">AddDumpInformationFile</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient4.md">IDebugClient4</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564611">.opendump (Open Dump File)</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient2.md">IDebugClient2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugClient::OpenDumpFile method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

