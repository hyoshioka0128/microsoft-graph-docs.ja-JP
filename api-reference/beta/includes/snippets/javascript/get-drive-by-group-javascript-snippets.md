---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1b79b5e0b9dc602917e38eb48ce4306643efef7e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503866"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{groupId}/drive')
    .version('beta')
    .get();

```