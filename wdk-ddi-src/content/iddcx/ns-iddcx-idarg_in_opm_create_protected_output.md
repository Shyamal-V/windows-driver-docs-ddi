---
UID: NS:iddcx.IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT
title: IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT
author: windows-driver-content
description: Gives information about the video output semantics for the OPM context that will be created.
old-location: display\idarg_in_opm_create_protected_output.htm
old-project: display
ms.assetid: c5727881-de35-4a61-bf54-0552d2de454b
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: iddcx/IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT, IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT, IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT structure [Display Devices], display.idarg_in_opm_create_protected_output
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iddcx.h
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
req.lib: 
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	iddcx.h
apiname:
-	IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT
product: Windows
targetos: Windows
req.typenames: 
---

# IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT structure


## -description


Gives information about the video output semantics for the OPM  context that will be created.
             


## -syntax


````
typedef struct IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT {
  OPM_VIDEO_OUTPUT_SEMANTICS VideoOutputSemantics;
} IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT, *IDARG_IN_OPM_CREATE_PROTECTED_OUTPUT;
````


## -struct-fields




### -field VideoOutputSemantics


                     [in] Type of video output semantics used for this context.

