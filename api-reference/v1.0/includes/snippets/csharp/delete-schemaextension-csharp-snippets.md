---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fc531ef720af87ba9a560a72b5efe39cc7fbcf1f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471405"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.SchemaExtensions["{id}"]
    .Request()
    .DeleteAsync();

```