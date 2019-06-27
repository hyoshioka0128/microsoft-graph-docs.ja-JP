---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ab70d7866c46080a2aae006af45c5518d66a806f
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/27/2019
ms.locfileid: "35333461"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/activities"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *itemActivityOLDList = [[NSMutableArray alloc] init];
        itemActivityOLDList = [jsonFinal valueForKey:@"value"];
        MSGraphItemActivityOLD *itemActivityOLD = [[MSGraphItemActivityOLD alloc] initWithDictionary:[itemActivityOLDList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```