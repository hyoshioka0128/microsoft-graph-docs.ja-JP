---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 4de6585f9984fb82ff12158bd477b98a2eaa85c0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504651"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var privilegedRoleAssignmentRequest = new PrivilegedRoleAssignmentRequest
{
    Duration = "2",
    Reason = "Activate the role for business purpose",
    TicketNumber = "234",
    TicketSystem = "system",
    Schedule = new GovernanceSchedule
    {
        StartDateTime = "2018-02-08T02:35:17.903Z"
    },
    EvaluateOnly = false,
    Type = "UserAdd",
    AssignmentState = "Active",
    RoleId = "88d8e3e3-8f55-4a1e-953a-9b9898b8876b"
};

await graphClient.PrivilegedRoleAssignmentRequests
    .Request()
    .AddAsync(privilegedRoleAssignmentRequest);

```