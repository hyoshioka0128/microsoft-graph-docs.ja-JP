---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c58224e5526d0b829237f782c169dfd0c1c7e0f3
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504500"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Drive.Root.Workbook.Worksheets["{id}"]
    .Range()
    .RowsBelow(count)
    .Request()
    .PostAsync();

```