---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 550f33e7dddda6e4b6a2134e5dd7611f8fab1f78
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464635"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/accessReviews/006111db-0810-4494-a6df-904d368bd81b"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphAccessReview *accessReview = [[MSGraphAccessReview alloc] init];
[accessReview setDisplayName:@"TestReview new name"];

NSError *error;
NSData *accessReviewData = [accessReview getSerializedDataWithError:&error];
[urlRequest setHTTPBody:accessReviewData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```