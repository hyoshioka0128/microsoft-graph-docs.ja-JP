---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d3e74f403f9c9e68546884dbef4e7fa542a76073
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503689"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getOneDriveUsageAccountDetail(period='D7')?$format=application/json"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *oneDriveUsageAccountDetailList = [[NSMutableArray alloc] init];
        oneDriveUsageAccountDetailList = [jsonFinal valueForKey:@"value"];
        MSGraphOneDriveUsageAccountDetail *oneDriveUsageAccountDetail = [[MSGraphOneDriveUsageAccountDetail alloc] initWithDictionary:[oneDriveUsageAccountDetailList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```