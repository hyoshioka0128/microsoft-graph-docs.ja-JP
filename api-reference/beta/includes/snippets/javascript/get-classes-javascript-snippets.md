---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 20d00a3a409947eb09400d19160a3f37bd62a851
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526167"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/me/classes')
    .version('beta')
    .get();

```