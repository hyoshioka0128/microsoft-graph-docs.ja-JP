---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 64fd80e19e377e51123ac066f4369960e4246cc6
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486539"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookTableRow = new WorkbookTableRow
{
    Index = 99,
    Values = "values-value"
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Rows["{index}"]
    .Request()
    .UpdateAsync(workbookTableRow);

```