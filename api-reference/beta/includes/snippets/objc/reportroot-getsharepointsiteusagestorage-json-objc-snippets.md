---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ad33d0fe4fba7799d555974f76e5f882e5229159
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485722"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getSharePointSiteUsageStorage(period='D7')?$format=application/json"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *siteUsageStorageList = [[NSMutableArray alloc] init];
        siteUsageStorageList = [jsonFinal valueForKey:@"value"];
        MSGraphSiteUsageStorage *siteUsageStorage = [[MSGraphSiteUsageStorage alloc] initWithDictionary:[siteUsageStorageList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```