---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2b770483d18be5bca7f92759e50b4406095d9213
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503455"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = new Attachment
{
    Name = "Personal pictures",
    SourceUrl = "https://contoso.com/personal/mario_contoso_net/Documents/Pics",
    ProviderType = "oneDriveConsumer",
    Permission = "Edit",
    IsFolder = "True"
};

await graphClient.Groups["c75831bdfad"].Threads["AAQkAGF97XEKhULw"].Posts["AAMkAGFcAAA"].Attachments
    .Request()
    .AddAsync(attachment);

```