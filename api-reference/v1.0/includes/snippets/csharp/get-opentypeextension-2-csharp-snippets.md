---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1b7723a6b564b34551c1ee4f91bf2a5ae3d02b7c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513674"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var extension = await graphClient.Groups["f5480dfd-7d77-4d0b-ba2e-3391953cc74a"].Events["AAMkADVl17IsAAA="].Extensions["Com.Contoso.Deal"]
    .Request()
    .GetAsync();

```