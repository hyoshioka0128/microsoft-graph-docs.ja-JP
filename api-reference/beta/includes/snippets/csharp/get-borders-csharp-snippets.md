---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2bfd99aa7ac1df716af1f090afd3233f64043416
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504030"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var borders = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"].Range().Format.Borders
    .Request()
    .GetAsync();

```