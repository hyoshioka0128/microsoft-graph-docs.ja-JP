---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 4f601e69eae0eb0bec735a8cc16dfdc1645398b2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514351"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const apply = {
  fields: [
    {
      key: 99,
      sortOn: "sortOn-value",
      ascending: true,
      color: "color-value",
      dataOption: "dataOption-value",
      icon: {
        set: "set-value",
        index: 99
      }
    }
  ],
  matchCase: true,
  hasHeaders: true,
  orientation: "orientation-value",
  method: "method-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/sort/apply')
    .post(apply);

```