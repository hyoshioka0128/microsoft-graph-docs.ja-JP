---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 81a8c6be7627fdb048e997e452f111ef6798c170
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527731"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/mailFolders/AAMkAGVmMDEzM/childFolders')
    .version('beta')
    .get();

```