---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3c31a90697c38a852017ea9acc45af1d9fb14722
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526531"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/planner/all/delta')
    .version('beta')
    .get();

```