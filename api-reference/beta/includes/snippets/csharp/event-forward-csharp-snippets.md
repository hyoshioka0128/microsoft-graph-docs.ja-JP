---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c90baf78633007b25810abc663b275d62045c60a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526382"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var toRecipients = new List<Recipient>()
{
    new Recipient
    {
        EmailAddress = new EmailAddress
        {
            Address = "danas@contoso.onmicrosoft.com",
            Name = "Dana Swope"
        }
    }
};

var comment = "Dana, hope you can make this meeting.";

await graphClient.Me.Events["{id}"]
    .Forward(comment,toRecipients)
    .Request()
    .PostAsync();

```