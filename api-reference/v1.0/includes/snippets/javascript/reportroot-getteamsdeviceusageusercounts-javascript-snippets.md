---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a40c07c0f4e7ec430f7d4c86aa09415405be9490
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471623"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getTeamsDeviceUsageUserCounts(period='D7')')
    .get();

```