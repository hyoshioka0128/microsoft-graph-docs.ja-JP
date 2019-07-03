---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: faad96f6eb25824e25bdf157852aa8c8d45da16e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487219"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const tiIndicator = {
  action: "alert",
  activityGroupNames: [],
  confidence: 0,
  description: "This is a canary indicator for demo purpose. Take no action on any observables set in this indicator.",
  expirationDateTime: "2019-03-01T21:43:37.5031462+00:00",
  externalId: "Test--8586509942679764298MS501",
  fileHashType: "sha256",
  fileHashValue: "aa64428647b57bf51524d1756b2ed746e5a3f31b67cf7fe5b5d8a9daf07ca313",
  killChain: [],
  malwareFamilyNames: [],
  severity: 0,
  tags: [],
  targetProduct: "Azure Sentinel",
  threatType: "WatchList",
  tlpLevel: "green"
};

let res = await client.api('/security/tiIndicators')
    .version('beta')
    .post({tiIndicator : tiIndicator});

```