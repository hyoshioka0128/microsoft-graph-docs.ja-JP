---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c42adf7624b652005db3647b20b44319b1b31038
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486665"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/chats/{id}/messages/{id}/hostedContents')
    .version('beta')
    .get();

```