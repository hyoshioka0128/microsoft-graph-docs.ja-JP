---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 8a54a4dd1aa8936f330bdbe651f08b8c46f6b20e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471327"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const notebook = {
  displayName: "Notebook name"
};

let res = await client.api('/me/onenote/notebooks')
    .post({notebook : notebook});

```