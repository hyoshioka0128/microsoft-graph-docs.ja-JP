---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 4e725439a65b27492f7e9abbe4590b529d341e3d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487138"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var contact = new Contact
{
    EmailAddresses = new List<TypedEmailAddress>()
    {
        new TypedEmailAddress
        {
            Type = EmailType.Personal,
            Name = "Pavel Bansky",
            Address = "pavelb@adatum.onmicrosoft.com"
        },
        new TypedEmailAddress
        {
            Address = "pavelb@fabrikam.onmicrosoft.com",
            Name = "Pavel Bansky",
            Type = EmailType.Other,
            OtherLabel = "Volunteer work"
        }
    }
};

await graphClient.Me.Contacts["AAMkADh6v5AAAvgTCEAAA="]
    .Request()
    .UpdateAsync(contact);

```