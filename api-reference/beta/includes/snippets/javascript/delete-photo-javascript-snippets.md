---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d636417de97e4c3a56392cd7b21de07ef33d31a3
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464686"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/users/{id|userPrincipalName}/photo')
    .version('beta')
    .delete();

```