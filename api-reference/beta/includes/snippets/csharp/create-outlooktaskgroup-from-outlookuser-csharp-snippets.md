---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: af60d1a2fe413e0cfec526e39d17116425aa6c8c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526023"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var outlookTaskGroup = new OutlookTaskGroup
{
    Name = "Leisure tasks"
};

await graphClient.Me.Outlook.TaskGroups
    .Request()
    .AddAsync(outlookTaskGroup);

```