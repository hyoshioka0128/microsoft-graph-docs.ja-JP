---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f12a47f2883fdd42ef1d2e257f65328ae548d553
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526344"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const CommsOperation = {
  clientContext: "clientContext-value"
};

let res = await client.api('/app/calls/{id}/mute')
    .version('beta')
    .post(CommsOperation);

```