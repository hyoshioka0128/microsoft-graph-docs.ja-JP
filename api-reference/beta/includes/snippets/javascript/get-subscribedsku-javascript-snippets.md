---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9802016782c35e635b31e0409cb0f79a26899ea2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527450"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/subscribedSkus/{id}')
    .version('beta')
    .get();

```