---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: cbd71f1137e25ff96640d98d58536f5a4811980d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527856"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const calendar = {
  name: "Social events"
};

let res = await client.api('/me/calendar')
    .version('beta')
    .update({calendar : calendar});

```