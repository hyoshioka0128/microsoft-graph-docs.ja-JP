---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e1433cf43a22e8f3354c05744d25c5b313933cde
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486699"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getSkypeForBusinessActivityUserDetail(period='D7')?$format=application/json"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *skypeForBusinessActivityUserDetailList = [[NSMutableArray alloc] init];
        skypeForBusinessActivityUserDetailList = [jsonFinal valueForKey:@"value"];
        MSGraphSkypeForBusinessActivityUserDetail *skypeForBusinessActivityUserDetail = [[MSGraphSkypeForBusinessActivityUserDetail alloc] initWithDictionary:[skypeForBusinessActivityUserDetailList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```