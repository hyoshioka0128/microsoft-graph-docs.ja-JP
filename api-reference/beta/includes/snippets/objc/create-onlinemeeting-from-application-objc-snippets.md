---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 76863c22526585db16e784a3ce986afc99922ef8
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503941"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/app/onlineMeetings"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphOnlineMeeting *OnlineMeeting = [[MSGraphOnlineMeeting alloc] init];
[OnlineMeeting setMeetingType: [MSGraphMeetingType MeetNow]];
MSGraphMeetingParticipants *participants = [[MSGraphMeetingParticipants alloc] init];
MSGraphMeetingParticipantInfo *organizer = [[MSGraphMeetingParticipantInfo alloc] init];
MSGraphIdentitySet *identity = [[MSGraphIdentitySet alloc] init];
MSGraphIdentity *user = [[MSGraphIdentity alloc] init];
[user setId:@"550fae72-d251-43ec-868c-373732c2704f"];
[identity setUser:user];
[organizer setIdentity:identity];
[participants setOrganizer:organizer];
[OnlineMeeting setParticipants:participants];
[OnlineMeeting setSubject:@"subject-value"];

NSError *error;
NSData *OnlineMeetingData = [OnlineMeeting getSerializedDataWithError:&error];
[urlRequest setHTTPBody:OnlineMeetingData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```