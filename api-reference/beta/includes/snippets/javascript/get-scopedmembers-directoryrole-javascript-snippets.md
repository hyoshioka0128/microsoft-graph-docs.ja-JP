---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 101e6b522909a2c7ab66c53a7149c6487612f55b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527728"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directoryRoles/{id}/scopedMembers')
    .version('beta')
    .get();

```