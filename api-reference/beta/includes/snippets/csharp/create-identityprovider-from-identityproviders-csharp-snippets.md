---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 268f21e78095874ec41dfa63d0bed37e825961c6
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464491"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var identityProvider = new IdentityProvider
{
    Name = "Login with Amazon",
    Type = "Amazon",
    ClientId = "56433757-cadd-4135-8431-2c9e3fd68ae8",
    ClientSecret = "000000000000"
};

await graphClient.IdentityProviders
    .Request()
    .AddAsync(identityProvider);

```