---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 66255c8734ce710555129cfb5b3a8253c4c7d41d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527419"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/onenote/operations/{id}')
    .version('beta')
    .get();

```