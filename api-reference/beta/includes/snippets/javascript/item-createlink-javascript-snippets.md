---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e06611a9dfcf9c4d067818939ad5fb0cc3cfe580
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504157"
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

let res = await client.api('/me/drive/items/{itemId}/createLink')
    .version('beta')
    .post(permission);

```