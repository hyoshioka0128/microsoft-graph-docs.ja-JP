---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d53144c379dfe36b6851a3d396699cddb54f8244
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527250"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/riskyUsers?$filter=riskLevel%20eq%20microsoft.graph.riskLevel'medium'"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *riskyUserList = [[NSMutableArray alloc] init];
        riskyUserList = [jsonFinal valueForKey:@"value"];
        MSGraphRiskyUser *riskyUser = [[MSGraphRiskyUser alloc] initWithDictionary:[riskyUserList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```