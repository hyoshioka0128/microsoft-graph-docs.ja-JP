---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d02dc44e6db9110fda137e65a1737729d42a713d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513661"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var list = new List
{
    DisplayName = "Books",
    Columns = new List<ColumnDefinition>()
    {
        new ColumnDefinition
        {
            Name = "Author",
            Text = new TextColumn
            {
            }
        },
        new ColumnDefinition
        {
            Name = "PageCount",
            Number = new NumberColumn
            {
            }
        }
    },
    List = new ListInfo
    {
        Template = "genericList"
    }
};

await graphClient.Sites["{site-id}"].Lists
    .Request()
    .AddAsync(list);

```