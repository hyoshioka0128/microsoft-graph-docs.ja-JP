---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 737dac64a7de1722ebff7f135d80a07c8165e2ba
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487233"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const sectionGroup = {
  displayName: "Section group name"
};

let res = await client.api('/me/onenote/sectionGroups/{id}/sectionGroups')
    .version('beta')
    .post({sectionGroup : sectionGroup});

```