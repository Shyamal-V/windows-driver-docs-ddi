---
UID: NF:portcls.IMiniportStreamAudioEngineNode.GetStreamChannelCount
title: IMiniportStreamAudioEngineNode::GetStreamChannelCount method
author: windows-driver-content
description: Gets a count of the number of channels available for the stream.
old-location: audio\iminiportstreamaudioenginenode_getstreamchannelcount.htm
old-project: audio
ms.assetid: D39376D8-CD1D-4E07-8017-0B552A4D2E59
ms.author: windowsdriverdev
ms.date: 2/8/2018
ms.keywords: GetStreamChannelCount, portcls/IMiniportStreamAudioEngineNode::GetStreamChannelCount, GetStreamChannelCount method [Audio Devices], IMiniportStreamAudioEngineNode interface [Audio Devices], GetStreamChannelCount method, IMiniportStreamAudioEngineNode, audio.iminiportstreamaudioenginenode_getstreamchannelcount, GetStreamChannelCount method [Audio Devices], IMiniportStreamAudioEngineNode interface, IMiniportStreamAudioEngineNode::GetStreamChannelCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portcls.h
req.include-header: 
req.target-type: Universal
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
req.lib: portcls.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	Portcls.h
apiname:
-	IMiniportStreamAudioEngineNode.GetStreamChannelCount
product: Windows
targetos: Windows
req.typenames: "*PPC_EXIT_LATENCY, PC_EXIT_LATENCY"
---

# IMiniportStreamAudioEngineNode::GetStreamChannelCount method


## -description


Gets a count of the number of channels available for the stream.


## -syntax


````
NTSTATUS GetStreamChannelCount(
  [in]  eChannelTargetType targetType,
  [out] UINT32             *pulChannelCount
);
````


## -parameters




### -param targetType [in]

An <a href="..\portcls\ne-portcls-echanneltargettype.md">eChannelTargetType</a> enumerated value that specifies the  target node type.


### -param pulChannelCount [out]

The number of available channels.


## -returns



<b>GetStreamChannelCount</b> returns S_OK, if the call was successful. Otherwise, the method returns an appropriate error 

code.




## -see-also

<a href="..\portcls\nn-portcls-iminiportstreamaudioenginenode.md">IMiniportStreamAudioEngineNode</a>



<a href="..\portcls\ne-portcls-echanneltargettype.md">eChannelTargetType</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20IMiniportStreamAudioEngineNode::GetStreamChannelCount method%20 RELEASE:%20(2/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

