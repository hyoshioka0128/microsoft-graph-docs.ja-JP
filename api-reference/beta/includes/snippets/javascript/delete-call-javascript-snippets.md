---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 52de1a8d89cd21c6b24b3e062c28b3f80903908b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527420"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/app/calls/{id}')
    .version('beta')
    .delete();

```