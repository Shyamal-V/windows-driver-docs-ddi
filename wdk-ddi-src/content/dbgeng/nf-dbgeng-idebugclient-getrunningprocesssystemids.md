---
UID: NF:dbgeng.IDebugClient.GetRunningProcessSystemIds
title: IDebugClient::GetRunningProcessSystemIds method
author: windows-driver-content
description: The GetRunningProcessSystemIds method returns the process IDs for each running process.
old-location: debugger\getrunningprocesssystemids.htm
old-project: debugger
ms.assetid: 6e7b6d54-e53b-4861-b888-ea63e3859139
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugClient3 interface [Windows Debugging], GetRunningProcessSystemIds method, GetRunningProcessSystemIds method [Windows Debugging], IDebugClient interface, IDebugClient5 interface [Windows Debugging], GetRunningProcessSystemIds method, IDebugClient interface [Windows Debugging], GetRunningProcessSystemIds method, dbgeng/IDebugClient5::GetRunningProcessSystemIds, IDebugClient, GetRunningProcessSystemIds method [Windows Debugging], GetRunningProcessSystemIds method [Windows Debugging], IDebugClient2 interface, dbgeng/IDebugClient4::GetRunningProcessSystemIds, IDebugClient4::GetRunningProcessSystemIds, IDebugClient2 interface [Windows Debugging], GetRunningProcessSystemIds method, IDebugClient5::GetRunningProcessSystemIds, GetRunningProcessSystemIds method [Windows Debugging], IDebugClient5 interface, IDebugClient3::GetRunningProcessSystemIds, IDebugClient4 interface [Windows Debugging], GetRunningProcessSystemIds method, dbgeng/IDebugClient3::GetRunningProcessSystemIds, dbgeng/IDebugClient::GetRunningProcessSystemIds, GetRunningProcessSystemIds method [Windows Debugging], IDebugClient4 interface, dbgeng/IDebugClient2::GetRunningProcessSystemIds, IDebugClient_f1eed41f-b746-4eb6-b6db-8eef7ac89d6a.xml, debugger.getrunningprocesssystemids, IDebugClient::GetRunningProcessSystemIds, IDebugClient2::GetRunningProcessSystemIds, GetRunningProcessSystemIds method [Windows Debugging], IDebugClient3 interface, GetRunningProcessSystemIds
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
-	IDebugClient.GetRunningProcessSystemIds
-	IDebugClient2.GetRunningProcessSystemIds
-	IDebugClient3.GetRunningProcessSystemIds
-	IDebugClient4.GetRunningProcessSystemIds
-	IDebugClient5.GetRunningProcessSystemIds
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugClient::GetRunningProcessSystemIds method


## -description


The <b>GetRunningProcessSystemIds</b> method returns the process IDs for each running process.


## -syntax


````
HRESULT GetRunningProcessSystemIds(
  [in]            ULONG64 Server,
  [out, optional] PULONG  Ids,
  [in]            ULONG   Count,
  [out, optional] PULONG  ActualCount
);
````


## -parameters




### -param Server [in]

Specifies the process server to query for process IDs.  If <i>Server</i> is zero, the engine will return the process IDs of the processes running on the local computer.


### -param Ids [out, optional]

Receives the process IDs.  The size of this array is <i>Count</i>.  If <i>Ids</i> is <b>NULL</b>, this information is not returned.


### -param Count [in]

Specifies the number of process IDs the array <i>Ids</i> can hold.


### -param ActualCount [out, optional]

Receives the actual number of process IDs returned in <i>Ids</i>.


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



This method is available only for live user-mode debugging.

For more information about creating and attaching to live user-mode targets, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552020">Live User-Mode Targets</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff539237">ConnectProcessServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548243">GetRunningProcessDescription</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538150">AttachProcess</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient.md">IDebugClient</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548254">GetRunningProcessSystemIdByExecutableName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540055">CreateProcessAndAttach2</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient3.md">IDebugClient3</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient4.md">IDebugClient4</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient2.md">IDebugClient2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugClient::GetRunningProcessSystemIds method%20 RELEASE:%20(1/19/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

