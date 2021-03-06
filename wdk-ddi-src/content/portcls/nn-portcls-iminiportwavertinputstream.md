---
UID: NN:portcls.IMiniportWaveRTInputStream
title: IMiniportWaveRTInputStream
author: windows-driver-content
description: The IMiniportWaveRTInputStream interface represents the input wave stream that flows through a pin on the KS filter that wraps a WaveRT rendering or capture device. IMiniportWaveRTInputStream inherits from the IUnknown interface.
old-location: audio\iminiportwavertinputstream.htm
old-project: audio
ms.assetid: BF490F9C-C1CD-4AEE-A970-161C5BB3A523
ms.author: windowsdriverdev
ms.date: 2/8/2018
ms.keywords: audio.iminiportwavertinputstream, IMiniportWaveRTInputStream interface [Audio Devices], IMiniportWaveRTInputStream interface [Audio Devices], described, IMiniportWaveRTInputStream, portcls/IMiniportWaveRTInputStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: portcls.h
req.include-header: 
req.target-type: Windows
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
req.lib: Portcls.lib
req.dll: 
req.irql: PASSIVE_LEVEL
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	portcls.h
apiname:
-	IMiniportWaveRTInputStream
product: Windows
targetos: Windows
req.typenames: "*PPC_EXIT_LATENCY, PC_EXIT_LATENCY"
---

# IMiniportWaveRTInputStream interface


## -description


The <code>IMiniportWaveRTInputStream</code> interface represents the input wave stream that flows through a pin on the KS filter that wraps a WaveRT rendering or capture device. <code>IMiniportWaveRTInputStream</code> inherits from the <b>IUnknown</b> interface.

A driver can implement this interface for better coordination of audio dataflow from the driver to OS. If this interface is available on a capture stream, the OS uses methods on this interface to access data in the WaveRt buffer. 
     <code>IMiniportWaveRTInputStream</code> is supported in Windows 10 and later.

