---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 37ad10e6fc75882c4c6e8803561f5a07165de6d8
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495896"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"].PivotTables["{id}"]
    .Refresh()
    .Request()
    .PostAsync();

```