---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fc9a9b82fa4b3f09a29ce17be24672b772e1a9f8
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472525"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getTeamsUserActivityUserCounts(period='D7')')
    .get();

```