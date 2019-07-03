---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 73811234dfe2f8b956f99007f8be1946b722e74f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503881"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var device = new Device
{
    AccountEnabled = true,
    AlternativeSecurityIds = new List<AlternativeSecurityId>()
    {
        new AlternativeSecurityId
        {
            Type = 99,
            IdentityProvider = "identityProvider-value",
            Key = "base64Y3YxN2E1MWFlYw=="
        }
    },
    ApproximateLastSignInDateTime = "2016-10-19T10:37:00Z",
    DeviceId = "deviceId-value",
    DeviceMetadata = "deviceMetadata-value",
    DeviceVersion = 99
};

await graphClient.Devices
    .Request()
    .AddAsync(device);

```