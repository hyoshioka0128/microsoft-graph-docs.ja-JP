---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 77c709428266b4cd92323e5c9694285945016363
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471133"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/events/AAMkAGIAAAoZDOFAAA=')
    .header('Prefer','outlook.timezone="Pacific Standard Time"')
    .select('subject,body,bodyPreview,organizer,attendees,start,end,location')
    .get();

```