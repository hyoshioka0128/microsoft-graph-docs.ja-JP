---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 174d489a3e25e438d8b399e95f3832d4b947f8a6
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486037"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/mailFolders')
    .version('beta')
    .get();

```