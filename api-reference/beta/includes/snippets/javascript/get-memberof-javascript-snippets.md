---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: de4951d8c8ef3a2db535146aefbaea2cbda803b5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486227"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/contacts/{id}/memberOf')
    .version('beta')
    .get();

```