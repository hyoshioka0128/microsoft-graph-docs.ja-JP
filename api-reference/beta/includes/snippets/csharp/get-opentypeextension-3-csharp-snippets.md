---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: cb1d8ef71d6b0cfae7d3f911e042f807b2aeceff
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504415"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = await graphClient.Me.Messages["AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl==="]
    .Request()
    .Filter("id eq 'Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')")
    .Expand("extensions($filter=id%20eq%20'Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')")
    .GetAsync();

```