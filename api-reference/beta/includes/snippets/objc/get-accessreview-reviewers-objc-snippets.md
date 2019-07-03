---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 87a35baee9d1a7f4eb35723615924f6cd43c3644
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485188"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/accessReviews/2b83cc42-09db-46f6-8c6e-16fec466a82d/reviewers"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *accessReviewReviewerList = [[NSMutableArray alloc] init];
        accessReviewReviewerList = [jsonFinal valueForKey:@"value"];
        MSGraphAccessReviewReviewer *accessReviewReviewer = [[MSGraphAccessReviewReviewer alloc] initWithDictionary:[accessReviewReviewerList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```