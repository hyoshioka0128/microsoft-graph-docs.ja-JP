---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e40d5bc6ea8a495fa902cc8d3c66a3ca0d87e050
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504638"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/mailFolders/AAMkAGVmMDEzN')
    .version('beta')
    .get();

```