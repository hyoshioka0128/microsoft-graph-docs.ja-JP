---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 65cf70a7b0b2277e217ba9857f0806c2f8c8822b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472414"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var color = "color-value";

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Format.Fill
    .SetSolidColor(color)
    .Request()
    .PostAsync();

```