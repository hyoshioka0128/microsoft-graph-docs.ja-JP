---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e2041bd9f0bb76e8d4df20f7156c0e75d7b6d775
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514498"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const forceDelete = {
  disableUserAccounts: true
};

let res = await client.api('/domains/{id}/forceDelete')
    .version('beta')
    .post(forceDelete);

```