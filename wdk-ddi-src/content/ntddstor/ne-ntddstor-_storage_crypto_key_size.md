---
UID: NE:ntddstor._STORAGE_CRYPTO_KEY_SIZE
title: "_STORAGE_CRYPTO_KEY_SIZE"
author: windows-driver-content
description: The STORAGE_CRYPTO_KEY_SIZE enum returns the Size of the key in bits.
old-location: storage\storage_crypto_key_size.htm
old-project: storage
ms.assetid: C3E5CEC6-34A2-48DF-B963-677C69A97E0B
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: STORAGE_CRYPTO_KEY_SIZE, ntddstor/StorageCryptoKeySizeUnknown, storage.storage_crypto_key_size, StorageCryptoKeySize512Bits, ntddstor/StorageCryptoKeySize512Bits, StorageCryptoKeySize256Bits, *PSTORAGE_CRYPTO_KEY_SIZE, STORAGE_CRYPTO_KEY_SIZE, *PSTORAGE_CRYPTO_KEY_SIZE, StorageCryptoKeySizeUnknown, ntddstor/STORAGE_CRYPTO_KEY_SIZE, STORAGE_CRYPTO_KEY_SIZE enumeration [Storage Devices], StorageCryptoKeySize192Bits, ntddstor/StorageCryptoKeySize256Bits, _STORAGE_CRYPTO_KEY_SIZE, StorageCryptoKeySize128Bits, STORAGE_CRYPTO_KEY_SIZE, *PSTORAGE_CRYPTO_KEY_SIZE enumeration [Storage Devices], ntddstor/StorageCryptoKeySize192Bits, ntddstor/StorageCryptoKeySize128Bits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddstor.h
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
-	Ntddstor.h
apiname:
-	STORAGE_CRYPTO_KEY_SIZE, *PSTORAGE_CRYPTO_KEY_SIZE
product: Windows
targetos: Windows
req.typenames: "*PSTORAGE_CRYPTO_KEY_SIZE, STORAGE_CRYPTO_KEY_SIZE"
---

# _STORAGE_CRYPTO_KEY_SIZE enumeration


## -description


The <b>STORAGE_CRYPTO_KEY_SIZE</b> enum returns the Size of the key in bits.


## -syntax


````
typedef enum _STORAGE_CRYPTO_KEY_SIZE { 
  StorageCryptoKeySizeUnknown  = 0,
  StorageCryptoKeySize128Bits  = 1,
  StorageCryptoKeySize192Bits,
  StorageCryptoKeySize256Bits,
  StorageCryptoKeySize512Bits
} STORAGE_CRYPTO_KEY_SIZE, *PSTORAGE_CRYPTO_KEY_SIZE;
````


## -enum-fields




### -field StorageCryptoKeySizeUnknown

Reserved for system use.


### -field StorageCryptoKeySize128Bits

Reserved for system use.


### -field StorageCryptoKeySize192Bits

Reserved for system use.


### -field StorageCryptoKeySize256Bits

Reserved for system use.


### -field StorageCryptoKeySize512Bits

Reserved for system use.

