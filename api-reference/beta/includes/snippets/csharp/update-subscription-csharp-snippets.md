---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 07559c71a1afeee4818c5bc9cfe7dc47955d9d26
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486353"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var subscription = new Subscription
{
    ExpirationDateTime = "2016-11-22T18:23:45.9356913Z"
};

await graphClient.Subscriptions["{id}"]
    .Request()
    .UpdateAsync(subscription);

```