---
UID: NF:dbgeng.IDebugControl3.OpenLogFile
title: IDebugControl3::OpenLogFile method
author: windows-driver-content
description: The OpenLogFile method opens a log file that will receive output from the client objects.
old-location: debugger\openlogfile.htm
old-project: debugger
ms.assetid: aba8839e-4c44-4c10-8b6f-9f5832c12166
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugControl interface [Windows Debugging], OpenLogFile method, IDebugControl2 interface [Windows Debugging], OpenLogFile method, dbgeng/IDebugControl::OpenLogFile, IDebugControl3 interface [Windows Debugging], OpenLogFile method, IDebugControl3, OpenLogFile method [Windows Debugging], IDebugControl2 interface, IDebugControl_984f684e-c1c0-4819-b8ac-02718581c6ad.xml, OpenLogFile method [Windows Debugging], IDebugControl3 interface, debugger.openlogfile, OpenLogFile method [Windows Debugging], IDebugControl interface, IDebugControl::OpenLogFile, IDebugControl2::OpenLogFile, OpenLogFile, dbgeng/IDebugControl2::OpenLogFile, IDebugControl3::OpenLogFile, OpenLogFile method [Windows Debugging], IDebugControl, dbgeng/IDebugControl3::OpenLogFile, IDebugControl2
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
-	IDebugControl.OpenLogFile
-	IDebugControl2.OpenLogFile
-	IDebugControl3.OpenLogFile
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugControl3::OpenLogFile method


## -description


The <b>OpenLogFile</b>  method opens a log file that will receive output from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539140">client objects</a>.


## -syntax


````
HRESULT OpenLogFile(
  [in] PCSTR File,
  [in] BOOL  Append
);
````


## -parameters




### -param File [in]

Specifies the name of the log file.  <i>File</i> can include a relative or absolute path; relative paths are relative to the directory in which the debugger  was started.  If the file does not exist, it will be created.


### -param Append [in]

Specifies whether or not to append log messages to an existing log file.  If <b>TRUE</b>, log messages will be appended to the file; if <b>FALSE</b>, the contents of any existing file matching <i>File</i> are discarded.


## -returns



This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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



<b>OpenLogFile</b> and <b>OpenLogFileWide</b> behave the same way as <a href="https://msdn.microsoft.com/library/windows/hardware/ff553155">OpenLogFile2</a> and <b>OpenLogFile2Wide</b> with <i>Flags</i> set to DEBUG_LOG_APPEND if <i>Append</i> is <b>TRUE</b> and DEBUG_LOG_DEFAULT otherwise.

Only one log file can be open at a time.  If there is already a log file open, it will be closed.

For more information about log files, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560116">Using Input and Output</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff553155">OpenLogFile2</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol.md">IDebugControl</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol2.md">IDebugControl2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556734">SetLogMask</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539148">CloseLogFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564018">.logopen (Open Log File)</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547066">GetLogMask</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547016">GetLogFile</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol3.md">IDebugControl3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563986">.logappend (Append Log File)</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugControl::OpenLogFile method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

