---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: acb7edca2d277d15bedc413fee59066893e336a2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496092"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/root/children')
    .get();

```