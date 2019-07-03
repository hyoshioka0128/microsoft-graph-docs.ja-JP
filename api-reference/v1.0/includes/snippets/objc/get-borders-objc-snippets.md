---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 4be85351066b95348054537c96083a1a9a2cebc4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471839"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/names/{name}/range/format/borders"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *workbookRangeBorderList = [[NSMutableArray alloc] init];
        workbookRangeBorderList = [jsonFinal valueForKey:@"value"];
        MSGraphWorkbookRangeBorder *workbookRangeBorder = [[MSGraphWorkbookRangeBorder alloc] initWithDictionary:[workbookRangeBorderList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```