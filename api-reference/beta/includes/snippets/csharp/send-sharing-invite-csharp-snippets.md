---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e75c28942a50ea791787e701ef38b819478dcc28
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526252"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var recipients = new List<DriveRecipient>()
{
    new DriveRecipient
    {
        Email = "ryan@contoso.org"
    }
};

var message = "Here's the file that we're collaborating on.";

var requireSignIn = true;

var sendInvitation = true;

var roles = new List<String>()
{
    "write"
};

var password = "password123";

var expirationDateTime = 7/15/2018 2:00:00 PM;

await graphClient.Me.Drive.Items["{item-id}"]
    .Invite(requireSignIn,roles,sendInvitation,message,recipients,expirationDateTime,password)
    .Request()
    .PostAsync();

```