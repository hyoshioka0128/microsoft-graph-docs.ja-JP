---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9640b142a2673ba6a5ee0707885c3701b275901d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471641"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/mailboxSettings"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphMailboxSettings *mailboxSettings = [[MSGraphMailboxSettings alloc] init];
MSGraphAutomaticRepliesSetting *automaticRepliesSetting = [[MSGraphAutomaticRepliesSetting alloc] init];
[automaticRepliesSetting setStatus: [MSGraphAutomaticRepliesStatus scheduled]];
MSGraphDateTimeTimeZone *scheduledStartDateTime = [[MSGraphDateTimeTimeZone alloc] init];
[scheduledStartDateTime setDateTime: "2016-03-20T18:00:00"];
[scheduledStartDateTime setTimeZone:@"UTC"];
[automaticRepliesSetting setScheduledStartDateTime:scheduledStartDateTime];
MSGraphDateTimeTimeZone *scheduledEndDateTime = [[MSGraphDateTimeTimeZone alloc] init];
[scheduledEndDateTime setDateTime: "2016-03-28T18:00:00"];
[scheduledEndDateTime setTimeZone:@"UTC"];
[automaticRepliesSetting setScheduledEndDateTime:scheduledEndDateTime];
[mailboxSettings setAutomaticRepliesSetting:automaticRepliesSetting];

NSError *error;
NSData *mailboxSettingsData = [mailboxSettings getSerializedDataWithError:&error];
[urlRequest setHTTPBody:mailboxSettingsData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```