---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: b893b6519c45e1dc5269f34173c9ed13bcf999d7
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514109"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var me = await graphClient.Me
    .Request()
    .Select( e => new {
             e.MailboxSettings 
             })
    .GetAsync();

var automaticRepliesSetting = me.MailboxSettings.AutomaticRepliesSetting;

```