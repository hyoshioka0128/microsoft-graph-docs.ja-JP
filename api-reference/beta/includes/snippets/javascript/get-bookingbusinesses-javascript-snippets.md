---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a9b8cae5c796eddb52b507e63199176a2d3845ef
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526719"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/bookingBusinesses')
    .version('beta')
    .get();

```