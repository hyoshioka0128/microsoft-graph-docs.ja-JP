---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a0d18136d8f3b6aa6828cc4f72fcf3a8997612db
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513320"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getMailboxUsageMailboxCounts(period='D7')')
    .get();

```