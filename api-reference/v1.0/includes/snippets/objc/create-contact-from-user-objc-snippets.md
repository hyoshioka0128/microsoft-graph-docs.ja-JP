---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e916fb344b401dd1f298c14f77dbea3dabdeb70f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514134"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/contacts"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphContact *contact = [[MSGraphContact alloc] init];
[contact setGivenName:@"Pavel"];
[contact setSurname:@"Bansky"];
NSMutableArray *emailAddressesList = [[NSMutableArray alloc] init];
MSGraphEmailAddress *emailAddresses = [[MSGraphEmailAddress alloc] init];
[emailAddresses setAddress:@"pavelb@fabrikam.onmicrosoft.com"];
[emailAddresses setName:@"Pavel Bansky"];
[emailAddressesList addObject: emailAddresses];
[contact setEmailAddresses:emailAddressesList];
NSMutableArray *businessPhonesList = [[NSMutableArray alloc] init];
[businessPhonesList addObject: @"+1 732 555 0102"];
[contact setBusinessPhones:businessPhonesList];

NSError *error;
NSData *contactData = [contact getSerializedDataWithError:&error];
[urlRequest setHTTPBody:contactData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```