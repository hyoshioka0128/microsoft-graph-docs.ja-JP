---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: db05a1a1279e1647d4d1114a2016756a0658d9c4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486458"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getEmailActivityCounts = await graphClient.Reports.GetEmailActivityCounts('D7')
    .Request()
    .GetAsync();

```