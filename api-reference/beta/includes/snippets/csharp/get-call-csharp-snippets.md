---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f7b26893333fb502127daf0440e51a5e0efe44ff
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486638"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var Call = await graphClient.App.Calls["{id}"]
    .Request()
    .GetAsync();

```