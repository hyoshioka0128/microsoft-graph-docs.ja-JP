---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 735cd4b244a1d97dfd3bf3a7a4044c6496c409be
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495909"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getYammerGroupsActivityGroupCounts(period='D7')')
    .get();

```