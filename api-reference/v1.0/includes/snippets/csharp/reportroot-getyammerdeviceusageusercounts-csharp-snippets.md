---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e8e9e9fce038a41558238d6dde6972834da395b1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471287"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var report = await graphClient.Reports.GetYammerDeviceUsageUserCounts('D7')
    .Request()
    .GetAsync();

```