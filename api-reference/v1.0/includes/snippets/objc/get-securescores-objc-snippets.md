---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d973ac397e4928df9be8d832dbc9649f279cf9c5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495487"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/security/secureScores?$top=1"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *secureScoreList = [[NSMutableArray alloc] init];
        secureScoreList = [jsonFinal valueForKey:@"value"];
        MSGraphSecureScore *secureScore = [[MSGraphSecureScore alloc] initWithDictionary:[secureScoreList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```