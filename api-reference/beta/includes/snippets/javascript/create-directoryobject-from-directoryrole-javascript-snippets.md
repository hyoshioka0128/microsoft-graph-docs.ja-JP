---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 867146d91976e1beba55eb7bfd00924c7b0c426e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486076"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const directoryObject = {
  directoryObject: {
  }
};

let res = await client.api('/directoryRoles/{id}/members/$ref')
    .version('beta')
    .post({directoryObject : directoryObject});

```