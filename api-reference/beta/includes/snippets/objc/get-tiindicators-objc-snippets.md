---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 22cb24c203eb20bc7020e05d867b549d7a1ccec2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526761"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/security/tiIndicators"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *tiIndicatorList = [[NSMutableArray alloc] init];
        tiIndicatorList = [jsonFinal valueForKey:@"value"];
        MSGraphTiIndicator *tiIndicator = [[MSGraphTiIndicator alloc] initWithDictionary:[tiIndicatorList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```