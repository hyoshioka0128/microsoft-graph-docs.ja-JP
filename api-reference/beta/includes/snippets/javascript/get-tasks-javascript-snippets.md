---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3e81b97809112de09bbbb90ddd80024b44259ad2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527603"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/planner/tasks')
    .version('beta')
    .get();

```