---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 73c57c7fee03b2cc1fa0e9f3836df25e2891ef7b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486908"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/title')
    .version('beta')
    .get();

```