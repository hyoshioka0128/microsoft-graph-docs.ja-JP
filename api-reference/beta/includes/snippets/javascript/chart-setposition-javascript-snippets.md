---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 783f5e6ebeb8c4648023021473bffd1d5189fab0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504720"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const setPosition = {
  startCell: "startCell-value",
  endCell: "endCell-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setPosition')
    .version('beta')
    .post(setPosition);

```