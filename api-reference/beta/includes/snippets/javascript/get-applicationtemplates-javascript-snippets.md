---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ace51b29cd55ff6ee7d157012ee4df78de43264a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527796"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/applicationTemplates')
    .version('beta')
    .get();

```