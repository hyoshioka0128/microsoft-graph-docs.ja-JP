---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a8fb6a95928980c79cd2b7a0c7f4333075484738
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527278"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const fieldValueSet = {
    Color: "Fuchsia",
    Quantity: 934
};

let res = await client.api('/sites/{site-id}/lists/{list-id}/items/{item-id}/fields')
    .version('beta')
    .update({fieldValueSet : fieldValueSet});

```