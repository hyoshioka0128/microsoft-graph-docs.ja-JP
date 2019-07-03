---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 60d7d85d3367273f4dad478882924a14888a0adc
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485103"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/outlook/taskgroups/AAMkADIyAAAhrbe-AAA="]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphOutlookTaskGroup *outlookTaskGroup = [[MSGraphOutlookTaskGroup alloc] init];
[outlookTaskGroup setName:@"Personal Tasks"];

NSError *error;
NSData *outlookTaskGroupData = [outlookTaskGroup getSerializedDataWithError:&error];
[urlRequest setHTTPBody:outlookTaskGroupData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```