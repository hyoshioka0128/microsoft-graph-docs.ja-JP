---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: efbee63257a4527add53e837ee10a1d8e575f354
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504510"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var educationAssignmentResource = await graphClient.Education.Classes["11021"].Assignments["19002"].Resources["22002"]
    .Request()
    .GetAsync();

```