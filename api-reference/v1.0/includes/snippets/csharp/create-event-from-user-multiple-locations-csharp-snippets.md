---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e1a4aa6360d423ccd8af43d72ff5a577c28a93ad
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472114"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var @event = new Event
{
    Subject = "Plan summer company picnic",
    Body = new ItemBody
    {
        ContentType = BodyType.Html,
        Content = "Let's kick-start this event planning!"
    },
    Start = new DateTimeTimeZone
    {
        DateTime = "2017-08-30T11:00:00",
        TimeZone = "Pacific Standard Time"
    },
    End = new DateTimeTimeZone
    {
        DateTime = "2017-08-30T12:00:00",
        TimeZone = "Pacific Standard Time"
    },
    Attendees = new List<Attendee>()
    {
        new Attendee
        {
            EmailAddress = new EmailAddress
            {
                Address = "DanaS@contoso.onmicrosoft.com",
                Name = "Dana Swope"
            },
            Type = AttendeeType.Required
        },
        new Attendee
        {
            EmailAddress = new EmailAddress
            {
                Address = "AlexW@contoso.onmicrosoft.com",
                Name = "Alex Wilber"
            },
            Type = AttendeeType.Required
        }
    },
    Location = new Location
    {
        DisplayName = "Conf Room 3; Fourth Coffee; Home Office",
        LocationType = LocationType.Default
    },
    Locations = new List<Location>()
    {
        new Location
        {
            DisplayName = "Conf Room 3"
        },
        new Location
        {
            DisplayName = "Fourth Coffee",
            Address = new PhysicalAddress
            {
                Street = "4567 Main St",
                City = "Redmond",
                State = "WA",
                CountryOrRegion = "US",
                PostalCode = "32008"
            },
            Coordinates = new OutlookGeoCoordinates
            {
                Latitude = 47.672,
                Longitude = -102.103
            }
        },
        new Location
        {
            DisplayName = "Home Office"
        }
    }
};

await graphClient.Me.Events
    .Request()
    .Header("Prefer","outlook.timezone=\"Pacific Standard Time\"")
    .AddAsync(@event);

```