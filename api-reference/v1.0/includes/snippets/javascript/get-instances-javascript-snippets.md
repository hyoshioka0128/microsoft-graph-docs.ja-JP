---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: bf2e45eb0cb73ebe11fc0ab0424a4d5ed0038e44
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472004"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/events/AAMkAGUzYRgWAAA=/instances?startDateTime=2019-04-08T09:00:00.0000000&endDateTime=2019-04-30T09:00:00.0000000&$select=subject,bodyPreview,seriesMasterId,type,recurrence,start,end')
    .select('subject,bodyPreview,seriesMasterId,type,recurrence,start,end')
    .get();

```