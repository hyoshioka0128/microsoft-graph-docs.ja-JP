---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 20759b72063bba3aa76f15d03e5a35ac10b5e41f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503897"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const synchronizationTemplate = {
    id: "Slack",
    applicationId: "{id}",
    factoryTag: "CustomSCIM"
};

let res = await client.api('/applications/{id}/synchronization/templates/{templateId}')
    .version('beta')
    .put({synchronizationTemplate : synchronizationTemplate});

```