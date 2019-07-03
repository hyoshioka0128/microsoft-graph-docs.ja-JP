---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fd7f5798d98521017bee7b162a725f2580c34bca
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485109"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/contacts/{id}"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphOrgContact *orgContact = [[MSGraphOrgContact alloc] init];
NSMutableArray *businessPhonesList = [[NSMutableArray alloc] init];
[businessPhonesList addObject: @"businessPhones-value"];
[orgContact setBusinessPhones:businessPhonesList];
[orgContact setCity:@"city-value"];
[orgContact setCompanyName:@"companyName-value"];
[orgContact setCountry:@"country-value"];
[orgContact setDepartment:@"department-value"];
[orgContact setDisplayName:@"displayName-value"];

NSError *error;
NSData *orgContactData = [orgContact getSerializedDataWithError:&error];
[urlRequest setHTTPBody:orgContactData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```