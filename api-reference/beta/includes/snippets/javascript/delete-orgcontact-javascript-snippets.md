---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 443d5ae391ca2140ea0bd1b70befd3cd615c2928
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504612"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/contacts/{id}')
    .version('beta')
    .delete();

```