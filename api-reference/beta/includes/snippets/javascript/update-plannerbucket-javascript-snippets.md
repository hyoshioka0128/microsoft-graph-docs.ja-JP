---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 740299c82a6679ac10476146c61290be9d975d0d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503752"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const plannerBucket = {
  name: "Development"
};

let res = await client.api('/planner/buckets/hsOf2dhOJkqyYYZEtdzDe2QAIUCR')
    .version('beta')
    .update({plannerBucket : plannerBucket});

```