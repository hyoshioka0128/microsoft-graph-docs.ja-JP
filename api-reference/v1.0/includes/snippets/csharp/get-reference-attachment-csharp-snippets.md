---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3ad19815e67b7c750a07bd7c9af22133657994e4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513629"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = await graphClient.Me.Messages["AAMkAGUzY5QKgAAA="].Attachments["AAMkAGUzY5QKgAAABEgAQAISJOe1FEqdNsMEQmpZjRW8="]
    .Request()
    .GetAsync();

```