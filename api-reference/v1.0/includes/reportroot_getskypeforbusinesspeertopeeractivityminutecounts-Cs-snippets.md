---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 86e6cc0fd8e410e41aa3df64398930965508d4d3
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34457391"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var report = await graphClient.Reports.GetSkypeForBusinessPeerToPeerActivityMinuteCounts('D7')
    .Request()
    .GetAsync();

```