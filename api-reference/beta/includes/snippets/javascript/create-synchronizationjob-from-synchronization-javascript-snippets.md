---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: eb125b9b027cdb5d3f27765065301830317cb82e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487229"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const synchronizationJob = {
    templateId: "BoxOutDelta"
};

let res = await client.api('/servicePrincipals/{id}/synchronization/jobs')
    .version('beta')
    .post({synchronizationJob : synchronizationJob});

```