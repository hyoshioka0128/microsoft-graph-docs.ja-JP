---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ba09b907027808a91b2823c030c7cc8fec942502
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527386"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/synchronizationProfiles/{id}/resume')
    .version('beta')
    .post();

```