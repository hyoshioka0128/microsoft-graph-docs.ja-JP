---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: cf2d284633e302e3d50f4d7572176789d8a2c99b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486461"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"].RejectedSenders.Reference
    .Request()
    .DeleteAsync();

```