---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d5f8ddb3e5c3dadf91625304cbcf6c672b19cbea
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485056"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/applications/{id}')
    .version('beta')
    .delete();

```