---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6b79cfc50b54a5babda4482320e7dd8924190524
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503775"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/schemaExtensions/{id}')
    .version('beta')
    .delete();

```