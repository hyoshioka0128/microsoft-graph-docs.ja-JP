---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6882a43d76f30f7f56d440be56668e8b9c588686
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514497"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/domains/{domain-name}/verify')
    .post();

```