---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: bac0f098e633c8839f11e356a4eb688e18c6192e
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34446506"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var scopedAdministratorOf = await graphClient.Me.ScopedAdministratorOf
    .Request()
    .GetAsync();

```