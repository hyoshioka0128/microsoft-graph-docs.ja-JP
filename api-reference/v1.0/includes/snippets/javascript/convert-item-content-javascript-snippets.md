---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 85433c1b5affc0c799315890f274d01a884a2f78
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495702"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{item-id}/content?format=%7Bformat%7D')
    .get();

```