---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: bdcb54069667118af908b12f588d7344d38c2967
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471651"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/secureScoreControlProfiles/{id}')
    .version('beta')
    .get();

```