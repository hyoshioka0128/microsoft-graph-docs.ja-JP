---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a6187c0d78ba5b7abb601b3c8fbabcbfda75c1d5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513473"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookWorksheet = new WorkbookWorksheet
{
    Position = 99,
    Name = "name-value",
    Visibility = "visibility-value"
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"]
    .Request()
    .UpdateAsync(workbookWorksheet);

```