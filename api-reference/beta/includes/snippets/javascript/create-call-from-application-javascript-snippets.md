---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: aa4e1c148a54777e566393d52f498bded0621827
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503626"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const Call = {
  callbackUri: "https://bot.contoso.com/api/calls",
  mediaConfig: {
    @odata.type: "#microsoft.graph.serviceHostedMediaConfig",
    preFetchMedia: [
      {
        uri: "https://cdn.contoso.com/beep.wav",
        resourceId: "1D6DE2D4-CD51-4309-8DAA-70768651088E"
      },
      {
        uri: "https://cdn.contoso.com/cool.wav",
        resourceId: "1D6DE2D4-CD51-4309-8DAA-70768651088F"
      }
    ]
  },
  source: {
    identity: {
      application: {
        id: "8A34A46B-3D17-4ADC-8DCE-DC4E7D572698"
      }
    },
    languageId: "languageId-value",
    region: "region-value"
  },
  subject: "Test Call",
  targets: [
    {
      identity: {
        user: {
          id: "550fae72-d251-43ec-868c-373732c2704f",
          tenantId: "72f988bf-86f1-41af-91ab-2d7cd011db47",
          displayName: "Heidi Steen"
        }
      }
    }
  ],
  tenantId: "tenantId-value"
};

let res = await client.api('/app/calls')
    .version('beta')
    .post({Call : Call});

```