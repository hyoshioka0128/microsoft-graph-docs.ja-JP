---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 29522765be4bbe5b7c35f46a2a0ffa7ca38f3f2c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464486"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var inferenceClassificationOverride = new InferenceClassificationOverride
{
    ClassifyAs = InferenceClassificationType.Focused,
    SenderEmailAddress = new EmailAddress
    {
        Name = "Samantha Booth",
        Address = "samanthab@adatum.onmicrosoft.com"
    }
};

await graphClient.Me.InferenceClassification.Overrides
    .Request()
    .AddAsync(inferenceClassificationOverride);

```