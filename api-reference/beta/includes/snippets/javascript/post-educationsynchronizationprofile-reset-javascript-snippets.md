---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 51bc86a97b9fc11e3e5dc14427d503abac3bdc68
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527388"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/synchronizationProfiles/{id}/reset')
    .version('beta')
    .post();

```