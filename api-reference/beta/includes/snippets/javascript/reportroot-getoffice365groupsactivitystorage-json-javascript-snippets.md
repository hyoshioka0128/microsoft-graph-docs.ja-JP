---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 7b2ba180bd8e4e0804880ba8c4e20e6300cecefb
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464670"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getOffice365GroupsActivityStorage(period='D7')')
    .version('beta')
    .get();

```