---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 7f91952574e1b5f8a215f53b2ef2afd1f68b687e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496311"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/range(address='A1:B2')')
    .get();

```