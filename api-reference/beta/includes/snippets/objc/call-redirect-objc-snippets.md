---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6f7cd72190f060ef467daf0371d68b49075ae254
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35525931"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/app/calls/{id}/redirect"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

NSMutableDictionary *payloadDictionary = [[NSMutableDictionary alloc] init];

NSMutableArray *targetsList = [[NSMutableArray alloc] init];
MSGraphInvitationParticipantInfo *targets = [[MSGraphInvitationParticipantInfo alloc] init];
[targets setEndpointType: [MSGraphEndpointType Default]];
MSGraphIdentitySet *identity = [[MSGraphIdentitySet alloc] init];
MSGraphIdentity *user = [[MSGraphIdentity alloc] init];
[user setId:@"550fae72-d251-43ec-868c-373732c2704f"];
[user setTenantId:@"72f988bf-86f1-41af-91ab-2d7cd011db47"];
[user setDisplayName:@"Heidi Steen"];
[identity setUser:user];
[targets setIdentity:identity];
[targets setLanguageId:@"en-US"];
[targets setRegion:@"westus"];
[targetsList addObject: targets];
payloadDictionary[@"targets"] = targetsList;

MSGraphCallDisposition *targetDisposition = [MSGraphCallDisposition Default];
payloadDictionary[@"targetDisposition"] = targetDisposition;

int32_t timeout = 99;
payloadDictionary[@"timeout"] = timeout;

BOOL maskCallee = NO;
payloadDictionary[@"maskCallee"] = maskCallee;

BOOL maskCaller = NO;
payloadDictionary[@"maskCaller"] = maskCaller;

NSData *data = [NSJSONSerialization dataWithJSONObject:payloadDictionary options:kNilOptions error:&error];
[urlRequest setHTTPBody:data];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```