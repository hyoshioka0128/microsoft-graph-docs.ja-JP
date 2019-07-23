---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: deb539663b9034f158b4e7e842f528b2087926c1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35525861"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getYammerGroupsActivityDetail(period='D7')?$format=text/csv"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *yammerGroupsActivityDetailList = [[NSMutableArray alloc] init];
        yammerGroupsActivityDetailList = [jsonFinal valueForKey:@"value"];
        MSGraphYammerGroupsActivityDetail *yammerGroupsActivityDetail = [[MSGraphYammerGroupsActivityDetail alloc] initWithDictionary:[yammerGroupsActivityDetailList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```