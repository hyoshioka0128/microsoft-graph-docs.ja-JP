---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: cffef970a55583a79202d9b31a5d0d75c8b535dd
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471183"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var teachers = await graphClient.Education.Classes["{class-id}"].Teachers
    .Request()
    .GetAsync();

```