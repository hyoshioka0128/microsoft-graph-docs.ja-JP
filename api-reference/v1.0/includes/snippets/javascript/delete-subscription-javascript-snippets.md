---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3cd9fa5a2348d10ca8c2c7171fe66b05628abf5d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495588"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/subscriptions/{id}')
    .delete();

```