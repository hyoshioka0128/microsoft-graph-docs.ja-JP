---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3905a2858b9089f1e4369db8a7480d6a4905678a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503773"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/administrativeUnits/{id}/scopedRoleMembers/{id}')
    .version('beta')
    .delete();

```