---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 76d991e826fcc8dc521bc0f0a14d214665567946
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486743"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const governanceRoleAssignmentRequest = {
  roleDefinitionId: "0e88fd18-50f5-4ee1-9104-01c3ed910065",
  resourceId: "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  subjectId: "74765671-9ca4-40d7-9e36-2f4a570608a6",
  assignmentState: "Eligible",
  type: "AdminExtend",
  reason: "extend role assignment",
  schedule: {
    type: "Once",
    startDateTime: "2018-05-12T23:53:55.327Z",
    endDateTime: "2018-08-10T23:53:55.327Z"
  }
};

let res = await client.api('/privilegedAccess/azureResources/roleAssignmentRequests')
    .version('beta')
    .post({governanceRoleAssignmentRequest : governanceRoleAssignmentRequest});

```