---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 91bfa373abf8a46f2793e5fcbbfdfa41bfe5469e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495749"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const event = {
  subject: "Let's go for lunch",
  body: {
    contentType: "HTML",
    content: "Does noon time work for you?"
  },
  start: {
      dateTime: "2017-09-04T12:00:00",
      timeZone: "Pacific Standard Time"
  },
  end: {
      dateTime: "2017-09-04T14:00:00",
      timeZone: "Pacific Standard Time"
  },
  recurrence: {
    pattern: {
      type: "weekly",
      interval: 1,
      daysOfWeek: [ "Monday" ]
    },
    range: {
      type: "endDate",
      startDate: "2017-09-04",
      endDate: "2017-12-31"
    }
  },
  location:{
      displayName:"Harry's Bar"
  },
  attendees: [
    {
      emailAddress: {
        address:"AdeleV@contoso.onmicrosoft.com",
        name: "Adele Vance"
      },
      type: "required"
    }
  ]
};

let res = await client.api('/me/events')
    .post({event : event});

```