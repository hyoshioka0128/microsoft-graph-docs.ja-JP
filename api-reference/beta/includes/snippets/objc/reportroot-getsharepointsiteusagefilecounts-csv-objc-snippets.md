---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 341294d12fb274103009917120860e8453d70d4b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485172"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getSharePointSiteUsageFileCounts(period='D7')?$format=text/csv"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *sharePointSiteUsageFileCountsList = [[NSMutableArray alloc] init];
        sharePointSiteUsageFileCountsList = [jsonFinal valueForKey:@"value"];
        MSGraphSharePointSiteUsageFileCounts *sharePointSiteUsageFileCounts = [[MSGraphSharePointSiteUsageFileCounts alloc] initWithDictionary:[sharePointSiteUsageFileCountsList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```