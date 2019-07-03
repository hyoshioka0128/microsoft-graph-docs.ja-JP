---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c8b93dda33b3011c18049426771d0cc1827de077
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486283"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/privilegedRoles"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *privilegedRoleList = [[NSMutableArray alloc] init];
        privilegedRoleList = [jsonFinal valueForKey:@"value"];
        MSGraphPrivilegedRole *privilegedRole = [[MSGraphPrivilegedRole alloc] initWithDictionary:[privilegedRoleList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```