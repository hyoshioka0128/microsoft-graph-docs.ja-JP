---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9db7d1e8565ac25c6ffbbcbd819713eae9342d83
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486790"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var calendarGroup = new CalendarGroup
{
    Name = "name-value",
    ClassId = "classId-value",
    ChangeKey = "changeKey-value"
};

await graphClient.Me.CalendarGroups
    .Request()
    .AddAsync(calendarGroup);

```