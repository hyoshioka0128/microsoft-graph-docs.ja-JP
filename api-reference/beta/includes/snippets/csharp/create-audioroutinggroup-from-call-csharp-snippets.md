---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 8af956d45ac54bc82405c6857c2bfe7caf5b8857
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486802"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var AudioRoutingGroup = new AudioRoutingGroup
{
    Id = "oneToOne",
    RoutingMode = RoutingMode.OneToOne,
    Sources = new List<String>()
    {
        "632899f8-2ea1-4604-8413-27bd2892079f"
    },
    Receivers = new List<String>()
    {
        "550fae72-d251-43ec-868c-373732c2704f"
    }
};

await graphClient.App.Calls["{id}"].AudioRoutingGroups
    .Request()
    .AddAsync(AudioRoutingGroup);

```