---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: aa38368f00ba725d180f9c4d6e7a6b93c7570795
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472360"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = new Message
{
    IsRead = "true"
};

await graphClient.Me.Messages["{id}"]
    .Request()
    .UpdateAsync(message);

```