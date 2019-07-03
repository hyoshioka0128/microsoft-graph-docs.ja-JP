---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d205496cccb064ea1be9000866e64c674bf8be32
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486255"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const privilegedRoleAssignmentRequest = {
    duration: "2",
    reason: "Activate the role for business purpose",
    ticketNumber: "234",
    ticketSystem: "system",
    schedule: {
        startDateTime: "2018-02-08T02:35:17.903Z"
    },
    evaluateOnly: false,
    type: "UserAdd",
    assignmentState: "Active",
    roleId: "88d8e3e3-8f55-4a1e-953a-9b9898b8876b"
};

let res = await client.api('/privilegedRoleAssignmentRequests')
    .version('beta')
    .post({privilegedRoleAssignmentRequest : privilegedRoleAssignmentRequest});

```