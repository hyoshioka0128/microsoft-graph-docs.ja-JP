---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 52a38fd810ddb7b620da211155c84160f6689fcc
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471563"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var itemAnalytics = await graphClient.Drives["{drive-id}"].Items["{item-id}"].Analytics
    .Request()
    .GetAsync();

```