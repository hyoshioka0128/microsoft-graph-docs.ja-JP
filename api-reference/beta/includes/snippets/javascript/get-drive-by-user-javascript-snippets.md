---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 068f01e8378e4f63cf7325052cb271a2ce7d8c68
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503863"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/users/{idOrUserPrincipalName}/drive')
    .version('beta')
    .get();

```