---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3161612c828c3b53c0fdb590561fa8c2542d1ee0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526268"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.AccessReviews["2975E9B5-44CE-4E71-93D3-30F03B5AA992"]
    .ApplyDecisions()
    .Request()
    .PostAsync();

```