---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 7df26e0895bc5f326c5ca7c2cbc27aaec68148d9
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527262"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getSharePointSiteUsageDetail(period='D7')')
    .version('beta')
    .get();

```