---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: bac0f098e633c8839f11e356a4eb688e18c6192e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35525882"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var scopedAdministratorOf = await graphClient.Me.ScopedAdministratorOf
    .Request()
    .GetAsync();

```