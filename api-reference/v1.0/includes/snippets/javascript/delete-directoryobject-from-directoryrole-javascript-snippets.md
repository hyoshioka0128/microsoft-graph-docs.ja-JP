---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f967ac07ded10f92892dbec3926a8532c86aa745
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514067"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directoryRoles/{id}/members/{id}/$ref')
    .delete();

```