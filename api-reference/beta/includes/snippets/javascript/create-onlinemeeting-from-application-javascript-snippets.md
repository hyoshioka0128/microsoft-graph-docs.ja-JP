---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 59747d0f9db174a15bdf57cbae6ec3adee872ba9
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486422"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const OnlineMeeting = {
  meetingType: "meetNow",
  participants: {
    organizer: {
      identity: {
        user: {
          id: "550fae72-d251-43ec-868c-373732c2704f"
        }
      }
    }
  },
  subject: "subject-value"
};

let res = await client.api('/app/onlineMeetings')
    .version('beta')
    .post({OnlineMeeting : OnlineMeeting});

```