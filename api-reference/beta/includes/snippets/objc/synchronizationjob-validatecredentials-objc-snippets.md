---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 21dbab30b12140ae10329e0f213426b99c2ba8e5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485425"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/servicePrincipals/{id}/synchronization/jobs/{id}/validateCredentials"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

NSMutableDictionary *payloadDictionary = [[NSMutableDictionary alloc] init];

NSMutableArray *credentialsList = [[NSMutableArray alloc] init];
MSGraphSynchronizationSecretKeyStringValuePair *credentials = [[MSGraphSynchronizationSecretKeyStringValuePair alloc] init];
[credentials setKey: [MSGraphSynchronizationSecret UserName]];
[credentials setValue:@"user@domain.com"];
[credentialsList addObject: credentials];
MSGraphSynchronizationSecretKeyStringValuePair *credentials = [[MSGraphSynchronizationSecretKeyStringValuePair alloc] init];
[credentials setKey: [MSGraphSynchronizationSecret Password]];
[credentials setValue:@"password-value"];
[credentialsList addObject: credentials];
payloadDictionary[@"credentials"] = credentialsList;

NSData *data = [NSJSONSerialization dataWithJSONObject:payloadDictionary options:kNilOptions error:&error];
[urlRequest setHTTPBody:data];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```