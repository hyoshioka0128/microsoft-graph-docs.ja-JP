---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 194aec85f4ca1704bab0e1c19ba52de4d0a4b89c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527218"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = new List<Site>()
{
    new Site
    {
        Id = "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740"
    },
    new Site
    {
        Id = "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851"
    }
};

await graphClient.Users["{user-id}"].FollowedSites
    .Remove(value)
    .Request()
    .PostAsync();

```