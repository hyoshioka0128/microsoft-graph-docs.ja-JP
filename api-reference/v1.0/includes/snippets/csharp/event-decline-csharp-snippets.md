---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: b51f7858ee54c5c7103444f112a56fa3b552375d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472084"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var comment = "comment-value";

var sendResponse = true;

await graphClient.Me.Events["{id}"]
    .Decline(comment,sendResponse)
    .Request()
    .PostAsync();

```