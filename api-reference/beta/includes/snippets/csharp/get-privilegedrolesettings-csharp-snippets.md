---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: b5b4312c65a8a42db6c33d9728a1bf84f7e99bc6
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486499"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var privilegedRoleSettings = await graphClient.PrivilegedRoles["{id}"].Settings
    .Request()
    .GetAsync();

```