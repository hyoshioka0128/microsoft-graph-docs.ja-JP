---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 8395d7d42c9636d18f517679436f63d7ee8c8d16
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514446"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Messages["{id}"]
    .Request()
    .DeleteAsync();

```