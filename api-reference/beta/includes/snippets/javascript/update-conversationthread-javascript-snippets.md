---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 15a8fab0d737bb34960c14ee6d2ebdd277221b8e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486027"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const conversationThread = {
  @odata.type:"#Microsoft.OutlookServices.ConversationThread",
  isLocked: true
};

let res = await client.api('/groups/{id}/threads/{id}')
    .version('beta')
    .update({conversationThread : conversationThread});

```