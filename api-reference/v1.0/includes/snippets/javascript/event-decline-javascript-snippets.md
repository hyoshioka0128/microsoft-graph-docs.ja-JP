---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6184f0d84f4ba099ecf0ec38e1cf52ccd019f9ab
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514548"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const decline = {
  comment: "comment-value",
  sendResponse: true
};

let res = await client.api('/me/events/{id}/decline')
    .post(decline);

```