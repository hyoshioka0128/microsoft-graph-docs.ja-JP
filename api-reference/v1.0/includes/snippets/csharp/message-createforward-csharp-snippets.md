---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 0ad8a5cb36b21cf6c88a9fd8000f9ba8bc4bd597
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514285"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Messages["{id}"]
    .CreateForward()
    .Request()
    .PostAsync();

```