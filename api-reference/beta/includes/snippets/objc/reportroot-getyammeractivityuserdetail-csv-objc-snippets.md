---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 0159deef2922464f0b7c4a8902f57239e86defe1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527761"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getYammerActivityUserDetail(period='D7')?$format=text/csv"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *yammerActivityUserDetailList = [[NSMutableArray alloc] init];
        yammerActivityUserDetailList = [jsonFinal valueForKey:@"value"];
        MSGraphYammerActivityUserDetail *yammerActivityUserDetail = [[MSGraphYammerActivityUserDetail alloc] initWithDictionary:[yammerActivityUserDetailList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```