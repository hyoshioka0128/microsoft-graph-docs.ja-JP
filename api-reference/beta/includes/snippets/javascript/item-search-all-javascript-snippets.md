---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: b52e605d9319f349c70317c22c4ec03586b784bc
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504155"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/search(q='{search-query}')')
    .version('beta')
    .get();

```