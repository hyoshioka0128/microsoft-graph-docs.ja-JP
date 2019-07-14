---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9fad3534f0128beaede524ce88e02479e83af720
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526233"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var shift = new Shift
{
    Id = "SHFT_577b75d2-a927-48c0-a5d1-dc984894e7b8",
    CreatedDateTime = "2019-03-14T04:32:51.451Z",
    LastModifiedDateTime = "2019-03-14T05:32:51.451Z",
    UserId = "c5d0c76b-80c4-481c-be50-923cd8d680a1",
    SchedulingGroupId = "TAG_228940ed-ff84-4e25-b129-1b395cf78be0",
    LastModifiedBy = new IdentitySet
    {
        Application = null,
        Device = null,
        Conversation = null,
        User = new Identity
        {
            Id = "366c0b19-49b1-41b5-a03f-9f3887bd0ed8",
            DisplayName = "John Doe"
        }
    },
    SharedShift = new ShiftItem
    {
        DisplayName = "Day shift",
        Notes = "Please do inventory as part of your shift.",
        StartDateTime = "2019-03-11T15:00:00Z",
        EndDateTime = "2019-03-12T00:00:00Z",
        Theme = ScheduleEntityTheme.Blue,
        Activities = new List<ShiftActivity>()
        {
            new ShiftActivity
            {
                IsPaid = true,
                StartDateTime = "2019-03-11T15:00:00Z",
                EndDateTime = "2019-03-11T15:15:00Z",
                Code = "",
                DisplayName = "Lunch"
            }
        }
    },
    DraftShift = new ShiftItem
    {
        DisplayName = "Day shift",
        Notes = "Please do inventory as part of your shift.",
        StartDateTime = "2019-03-11T15:00:00Z",
        EndDateTime = "2019-03-12T00:00:00Z",
        Theme = ScheduleEntityTheme.Blue,
        Activities = new List<ShiftActivity>()
        {
            new ShiftActivity
            {
                IsPaid = true,
                StartDateTime = "2019-03-11T15:00:00Z",
                EndDateTime = "2019-03-11T15:30:00Z",
                Code = "",
                DisplayName = "Lunch"
            }
        }
    }
};

await graphClient.Teams["{teamId}"].Schedule.Shifts["{shiftId}"]
    .Request()
    .Header("Prefer","return=representation")
    .PutAsync(shift);

```