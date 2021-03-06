---
UID: NF:stiusd.IStiDeviceControl.GetMyDevicePortName
title: IStiDeviceControl::GetMyDevicePortName method
author: windows-driver-content
description: The IStiDeviceControl::GetMyDevicePortName method allows a user-mode still image minidriver to obtain a device's port name.
old-location: image\istidevicecontrol_getmydeviceportname.htm
old-project: image
ms.assetid: f400ab05-aea9-4154-a725-5b23a6dc06b6
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: IStiDeviceControl::GetMyDevicePortName, IStiDeviceControl, GetMyDevicePortName, stiusd/IStiDeviceControl::GetMyDevicePortName, GetMyDevicePortName method [Imaging Devices], stifnc_00f6a8a0-b5dc-43d7-8a68-23b15592b404.xml, IStiDeviceControl interface [Imaging Devices], GetMyDevicePortName method, GetMyDevicePortName method [Imaging Devices], IStiDeviceControl interface, image.istidevicecontrol_getmydeviceportname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: stiusd.h
req.include-header: Stiusd.h
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
req.lib: stiusd.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	stiusd.h
apiname:
-	IStiDeviceControl.GetMyDevicePortName
product: Windows
targetos: Windows
req.typenames: "*PSTI_WIA_DEVICE_INFORMATIONW, STI_WIA_DEVICE_INFORMATIONW"
req.product: Windows 10 or later.
---

# IStiDeviceControl::GetMyDevicePortName method


## -description


The <b>IStiDeviceControl::GetMyDevicePortName</b> method allows a user-mode still image minidriver to obtain a device's port name.


## -syntax


````
HRESULT GetMyDevicePortName(
   LPWSTR lpszDevicePath,
   DWORD  cwDevicePathSize
);
````


## -parameters




### -param lpszDevicePath

Caller-supplied pointer to a buffer to receive the device's port name.


### -param cwDevicePathSize

Caller-supplied number of characters (of type TCHAR) in the buffer pointed to by <i>lpszDevicePath</i>.


## -returns



If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



The path name that a still image minidriver receives by calling <b>IStiDeviceControl::GetMyDevicePortName</b> can be used as an input argument to <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> (described in the Microsoft Windows SDK documentation).

A still image minidriver receives an <b>IStiDeviceControl</b> interface pointer as an input argument to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method.



