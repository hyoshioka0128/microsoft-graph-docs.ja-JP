---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3b569f2fd5cc8c60c6ea814a1420d920c3c10449
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504419"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var OnlineMeeting = await graphClient.App.OnlineMeetings["{id}"]
    .Request()
    .GetAsync();

```