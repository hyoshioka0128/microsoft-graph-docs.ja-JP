---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f8cff9f47239e09e570ab0c1af9a57a1893bed0d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35533585"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/calendarView/delta?startdatetime=2016-12-01T00:00:00Z&enddatetime=2016-12-30T00:00:00Z')
    .header('Prefer','odata.maxpagesize=2')
    .get();

```