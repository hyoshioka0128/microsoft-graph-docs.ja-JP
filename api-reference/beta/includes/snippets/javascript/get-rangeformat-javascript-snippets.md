---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f0d78e5654756f612e5819a8ab76982398665156
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504576"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/format')
    .version('beta')
    .get();

```