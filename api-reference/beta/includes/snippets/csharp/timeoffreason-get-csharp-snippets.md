---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d051e55d690f0385309bf211b1da8ddd6a50613a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527228"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var timeOffReason = await graphClient.Teams["{teamId}"].Schedule.TimeOffReasons["{timeOffReasonId}"]
    .Request()
    .GetAsync();

```