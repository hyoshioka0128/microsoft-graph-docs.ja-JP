---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3553749da5dcc97c16fa750569b2221a81773d1a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526454"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/planner/buckets/hsOf2dhOJkqyYYZEtdzDe2QAIUCR')
    .version('beta')
    .get();

```