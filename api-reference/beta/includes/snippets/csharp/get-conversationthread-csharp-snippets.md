---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: abbfb091f6ec6725e544267d46af2e1b06015d90
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504675"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conversationThread = await graphClient.Groups["{id}"].Threads["{id}"]
    .Request()
    .GetAsync();

```