---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: de8157b54b07d7e1b59ddb823662d651b60d6d58
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471777"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookRangeFont = new WorkbookRangeFont
{
    Italic = true,
    Size = 26
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{sheet-id}"].Range('$B$1').Format.Font
    .Request()
    .UpdateAsync(workbookRangeFont);

```