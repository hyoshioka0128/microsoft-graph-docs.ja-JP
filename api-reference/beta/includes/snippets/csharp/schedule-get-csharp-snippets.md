---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 668dd8b1a440b3a2d9e59df6fc41ac0b85ff80ae
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486124"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var schedule = await graphClient.Teams["{teamId}"].Schedule
    .Request()
    .GetAsync();

```