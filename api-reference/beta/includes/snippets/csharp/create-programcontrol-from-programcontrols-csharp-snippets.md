---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5d9ad6727ad4bb483bf9937cc660225521efd67d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503461"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var programControl = new ProgramControl
{
    ControlId = "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
    ControlTypeId = "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    ProgramId = "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213"
};

await graphClient.ProgramControls
    .Request()
    .AddAsync(programControl);

```