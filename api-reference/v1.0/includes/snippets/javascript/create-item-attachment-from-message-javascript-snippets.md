---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d1387ee74e1e53965dbdbebf5b95594f63460bcb
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471382"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const attachment = {
  @odata.type: "#microsoft.graph.itemAttachment",
  name: "Holiday event", 
  item: {
    @odata.type: "microsoft.graph.event",
    subject: "Discuss gifts for children",
    body: {
      contentType: "HTML",
      content: "Let's look for funding!"
    },
    start: {
      dateTime: "2016-12-02T18:00:00",
      timeZone: "Pacific Standard Time"
    },
    end: {
      dateTime: "2016-12-02T19:00:00",
      timeZone: "Pacific Standard Time"
    }
  }
};

let res = await client.api('/me/messages/AAMkpsDRVK/attachments')
    .post({attachment : attachment});

```