---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ef4a1a6a820fcb54c86e55824a80e98492bb69c3
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527398"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const String = {
  securityEnabledOnly: true
};

let res = await client.api('/contacts/{id}/getMemberObjects')
    .version('beta')
    .post(String);

```