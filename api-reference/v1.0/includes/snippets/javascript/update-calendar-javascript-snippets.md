---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 73d3f6f34a91250558f4d13e3a323198a7a46b15
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495780"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const calendar = {
  name: "Social events"
};

let res = await client.api('/me/calendar')
    .update({calendar : calendar});

```