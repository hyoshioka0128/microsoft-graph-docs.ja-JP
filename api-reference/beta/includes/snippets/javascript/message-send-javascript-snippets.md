---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9fe36f9bcfbc49c4fb72fbb9e6615066449befd0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486770"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages/{id}/send')
    .version('beta')
    .post();

```