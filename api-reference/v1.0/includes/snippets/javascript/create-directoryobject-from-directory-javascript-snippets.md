---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2899d5e46380611c0f266d35e0cc4d198289795b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471258"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directory/deletedItems/{object-id}/restore')
    .post();

```