---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ce5550bee3eb2891a59d7555733aa28ccec62319
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471300"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var report = await graphClient.Reports.GetTeamsUserActivityUserCounts('D7')
    .Request()
    .GetAsync();

```