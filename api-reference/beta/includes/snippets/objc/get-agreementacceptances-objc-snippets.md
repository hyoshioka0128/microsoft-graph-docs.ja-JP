---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 706c9e37b113440f3070abc57890f0a62939e0f7
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504354"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/agreementAcceptances"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *agreementAcceptanceList = [[NSMutableArray alloc] init];
        agreementAcceptanceList = [jsonFinal valueForKey:@"value"];
        MSGraphAgreementAcceptance *agreementAcceptance = [[MSGraphAgreementAcceptance alloc] initWithDictionary:[agreementAcceptanceList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```