---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 7dd8893c92b80de73694dbdcb936702920bf2abe
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504662"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"].Participants["{id}"]
    .Mute(clientContext)
    .Request()
    .PostAsync();

```