---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 02a8c0ce82175be422467ef9d9a86bd932eb24bb
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513736"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupSettings = await graphClient.GroupSettings
    .Request()
    .GetAsync();

```