---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: df4dde836ad98b32638caa830cd8711411ffbde2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503477"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailFolder = new MailFolder
{
    DisplayName = "displayName-value"
};

await graphClient.Me.MailFolders
    .Request()
    .AddAsync(mailFolder);

```