---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5d04ecfc79d7b5aa4d0899d1bb78447652d7b909
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486697"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/teams/{teamId}/schedule/timeOffReasons"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphTimeOffReason *timeOffReason = [[MSGraphTimeOffReason alloc] init];
[timeOffReason setDisplayName:@"Vacation"];
[timeOffReason setIconType: [MSGraphTimeOffReasonIconType plane]];
[timeOffReason setIsActive: true];

NSError *error;
NSData *timeOffReasonData = [timeOffReason getSerializedDataWithError:&error];
[urlRequest setHTTPBody:timeOffReasonData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```