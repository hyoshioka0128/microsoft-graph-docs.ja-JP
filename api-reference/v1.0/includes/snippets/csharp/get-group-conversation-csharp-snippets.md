---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 31db2893c05aab868ca58ccf0d3906f87d06c44e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514557"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conversation = await graphClient.Groups["02bd9fd6-8f93-4758-87c3-1fb73740a315"].Conversations["AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgAQABuXO3guDWBMpyKF7LsVwfU="]
    .Request()
    .GetAsync();

```