---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 39f0d86ddf3e1ce9a5a79a29fb506d572460e147
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472395"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getSharePointActivityFileCounts(period='D7')')
    .get();

```