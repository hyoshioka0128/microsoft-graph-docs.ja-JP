---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 7cea20cb1472738691fd730d4bd0ebcf3a56aa62
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514118"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var list = await graphClient.Sites["{site-id}"].Lists["{list-id}"]
    .Request()
    .GetAsync();

```