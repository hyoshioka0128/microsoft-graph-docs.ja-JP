---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6527db1e365142a28a3846a34415b32efca78701
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504001"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const program = {
    displayName: "testprogram3 new name"
};

let res = await client.api('/programs/7e59d237-2fb0-4e5d-b7bb-d4f9f9129213')
    .version('beta')
    .update({program : program});

```