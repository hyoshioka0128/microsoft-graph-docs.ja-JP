---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 023567465bf108d68f1bd3cc60e16520cca2fb1b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485723"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getSharePointSiteUsageSiteCounts(period='D7')?$format=text/csv"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *sharePointSiteUsageSiteCountsList = [[NSMutableArray alloc] init];
        sharePointSiteUsageSiteCountsList = [jsonFinal valueForKey:@"value"];
        MSGraphSharePointSiteUsageSiteCounts *sharePointSiteUsageSiteCounts = [[MSGraphSharePointSiteUsageSiteCounts alloc] initWithDictionary:[sharePointSiteUsageSiteCountsList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```