---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 19a31bd49fcc9dc96a215f6e0c45a6a0f533786f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485331"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Education.Classes["11021"].Assignments["19002"].Submissions["850f51b7"]
    .Unsubmit()
    .Request()
    .PostAsync();

```