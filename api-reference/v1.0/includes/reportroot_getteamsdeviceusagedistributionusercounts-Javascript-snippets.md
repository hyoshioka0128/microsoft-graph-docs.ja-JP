---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: bdcfa9a060f694326f27f49a78954cc755a71ebc
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34434921"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')')
    .get();

```