---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 80241ef7fc85772546addae5df2d823462ac490c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527852"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/calendars/AAMkAGViNDU7zAAAAAGtlAAA=/events"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphEvent *event = [[MSGraphEvent alloc] init];
[event setSubject:@"Let's go for lunch"];
MSGraphItemBody *body = [[MSGraphItemBody alloc] init];
[body setContentType: [MSGraphBodyType html]];
[body setContent:@"Does next month work for you?"];
[event setBody:body];
MSGraphDateTimeTimeZone *start = [[MSGraphDateTimeTimeZone alloc] init];
[start setDateTime: "2019-03-10T12:00:00"];
[start setTimeZone:@"Pacific Standard Time"];
[event setStart:start];
MSGraphDateTimeTimeZone *end = [[MSGraphDateTimeTimeZone alloc] init];
[end setDateTime: "2019-03-10T14:00:00"];
[end setTimeZone:@"Pacific Standard Time"];
[event setEnd:end];
MSGraphLocation *location = [[MSGraphLocation alloc] init];
[location setDisplayName:@"Harry's Bar"];
[event setLocation:location];
NSMutableArray *attendeesList = [[NSMutableArray alloc] init];
MSGraphAttendee *attendees = [[MSGraphAttendee alloc] init];
MSGraphEmailAddress *emailAddress = [[MSGraphEmailAddress alloc] init];
[emailAddress setAddress:@"adelev@contoso.onmicrosoft.com"];
[emailAddress setName:@"Adele Vance"];
[attendees setEmailAddress:emailAddress];
[attendees setType: [MSGraphAttendeeType required]];
[attendeesList addObject: attendees];
[event setAttendees:attendeesList];

NSError *error;
NSData *eventData = [event getSerializedDataWithError:&error];
[urlRequest setHTTPBody:eventData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```