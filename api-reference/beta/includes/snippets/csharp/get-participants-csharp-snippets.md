---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e7f12dbc19a85b50c58ddcb69e24b7ad05edec1a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527109"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var participants = await graphClient.App.Calls["57DAB8B1894C409AB240BD8BEAE78896"].Participants
    .Request()
    .Header("Authorization","Bearer <TOKEN>")
    .GetAsync();

```