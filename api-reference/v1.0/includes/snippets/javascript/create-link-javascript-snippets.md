---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 214953ab3b3bcba417f4f92915bf8e3da90c5d00
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513818"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const permission = {
  type: "view",
  scope: "anonymous"
};

let res = await client.api('/me/drive/items/{item-id}/createLink')
    .post(permission);

```