---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6b24b5a391f601c9f73042f608b9ef7992b7d367
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485934"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getYammerActivityCounts(period='D7')')
    .version('beta')
    .get();

```