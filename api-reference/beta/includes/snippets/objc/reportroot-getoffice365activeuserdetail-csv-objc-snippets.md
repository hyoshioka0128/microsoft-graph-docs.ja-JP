---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9adb974975a6f5f24f10183960a6e3aac6d8e3e4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503492"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getOffice365ActiveUserDetail(period='D7')?$format=text/csv"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *office365ActiveUserDetailList = [[NSMutableArray alloc] init];
        office365ActiveUserDetailList = [jsonFinal valueForKey:@"value"];
        MSGraphOffice365ActiveUserDetail *office365ActiveUserDetail = [[MSGraphOffice365ActiveUserDetail alloc] initWithDictionary:[office365ActiveUserDetailList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```