---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f04a543d91344345401916d600f10acea89bfed5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503787"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Root.Items.{item-id}.Permissions.{perm-id}
    .Request()
    .DeleteAsync();

```