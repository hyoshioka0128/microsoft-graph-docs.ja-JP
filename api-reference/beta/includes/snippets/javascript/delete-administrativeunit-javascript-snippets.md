---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1b1e2d4aa138ffc0cece092808ee757e88c75819
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485060"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/administrativeUnits/{id}')
    .version('beta')
    .delete();

```