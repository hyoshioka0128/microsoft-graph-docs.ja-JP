---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 14c5c1e6d7860a659ffbbf99e2c0f5459e27cbb1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495652"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var comment = "comment-value";

await graphClient.Me.Messages["{id}"]
    .ReplyAll(comment)
    .Request()
    .PostAsync();

```