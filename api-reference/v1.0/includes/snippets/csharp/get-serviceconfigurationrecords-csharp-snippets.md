---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: b617e5f2335751e9c90345202daff4d20a93d67a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513722"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var serviceConfigurationRecords = await graphClient.Domains["{domain-name}"].ServiceConfigurationRecords
    .Request()
    .GetAsync();

```