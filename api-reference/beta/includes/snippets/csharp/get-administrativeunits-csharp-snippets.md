---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 762704527d002291e1012a30651f7712933a0977
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526378"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var administrativeUnits = await graphClient.AdministrativeUnits
    .Request()
    .GetAsync();

```