---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2908594ae5b2d6fb57e55b2bf69560f4b8e92b5e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513190"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const String = {
  securityEnabledOnly: true
};

let res = await client.api('/me/getMemberGroups')
    .post(String);

```