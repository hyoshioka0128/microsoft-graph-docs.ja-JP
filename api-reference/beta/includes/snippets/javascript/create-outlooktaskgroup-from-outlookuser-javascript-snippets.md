---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2f6100df948bed777cff84b9f151585c727a9c5f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486414"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const outlookTaskGroup = {
  name: "Leisure tasks"
};

let res = await client.api('/me/outlook/taskGroups')
    .version('beta')
    .post({outlookTaskGroup : outlookTaskGroup});

```