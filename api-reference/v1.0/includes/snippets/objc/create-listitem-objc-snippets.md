---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a2c041cc4416e88de9b439361b39b6e26c4b73a1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514001"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/sites/{site-id}/lists/{list-id}/items"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphListItem *listItem = [[MSGraphListItem alloc] init];
MSGraphFieldValueSet *fields = [[MSGraphFieldValueSet alloc] init];
[fields setTitle:@"Widget"];
[fields setColor:@"Purple"];
[fields setWeight: 32];
[listItem setFields:fields];

NSError *error;
NSData *listItemData = [listItem getSerializedDataWithError:&error];
[urlRequest setHTTPBody:listItemData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```