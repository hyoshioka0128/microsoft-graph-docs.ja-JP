---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e50387b197d68ee44a79cde6a84e5af7ffe0cb05
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464542"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts')
    .version('beta')
    .get();

```