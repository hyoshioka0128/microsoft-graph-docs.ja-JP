---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5a4b8f0697c1000ceafef237c88289a8ea0e4a35
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464453"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Activities["13881113971988980728"]
    .Request()
    .DeleteAsync();

```