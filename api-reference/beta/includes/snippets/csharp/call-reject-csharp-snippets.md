---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a6d695c7d6c77ffdf70761d2c57e1c5dd9a9b810
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485818"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var reason = RejectReason.None;

await graphClient.App.Calls["{id}"]
    .Reject(reason)
    .Request()
    .PostAsync();

```