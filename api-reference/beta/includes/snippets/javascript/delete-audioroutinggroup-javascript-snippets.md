---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 41ee69e2efdbcca998c34cfac20edfafcec64437
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485051"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/app/calls/{id}/audioRoutingGroups/{id}')
    .version('beta')
    .delete();

```