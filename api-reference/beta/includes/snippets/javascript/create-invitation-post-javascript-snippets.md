---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 70f9fbb6c8758631cb51618b6101a2f37c3ba149
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486454"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const invitation = {
  invitedUserEmailAddress: "yyy@test.com",
  inviteRedirectUrl: "https://myapp.com"
};

let res = await client.api('/invitations')
    .version('beta')
    .post({invitation : invitation});

```