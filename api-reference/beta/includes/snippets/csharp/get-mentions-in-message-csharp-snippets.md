---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6b3037e8a7f3143ebaae1864336e01fe1fe142f0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526635"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = await graphClient.Me.Messages["AQMkADJmMTUAAAgVZAAAA"]
    .Request()
    .Expand("mentions")
    .GetAsync();

```