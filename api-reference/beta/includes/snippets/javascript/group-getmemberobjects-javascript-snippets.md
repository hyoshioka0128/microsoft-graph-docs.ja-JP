---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: dd54707a480ffc5b3c6ce4dfbf933b475d6f5358
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527136"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const String = {
  securityEnabledOnly: false
};

let res = await client.api('/groups/{id}/getMemberObjects')
    .version('beta')
    .post(String);

```