---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5a7e0ea0abfa0c927ca9f913693fd85feb3a7559
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503502"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/secureScores')
    .version('beta')
    .top(1)
    .get();

```