---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: be724dadca7b6fc2c5c11cc653349b51f4dc997f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496130"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var delta = await graphClient.Me.MailFolders["{id}"].Messages.Delta()
    .Request()
    .Header("Prefer","odata.maxpagesize=2")
    .GetAsync();

```