---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 43c63a9b10f7e1c08d25dd68241af07a30d20930
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526246"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>()
{
    "groupIds-value"
};

await graphClient.ServicePrincipals["{id}"]
    .CheckMemberGroups(groupIds)
    .Request()
    .PostAsync();

```