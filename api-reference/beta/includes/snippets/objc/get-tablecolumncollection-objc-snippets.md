---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 676bbed81ce0d2491d5c51578a1199992b0049f7
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526664"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/tables/{id|name}/columns"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *workbookTableColumnList = [[NSMutableArray alloc] init];
        workbookTableColumnList = [jsonFinal valueForKey:@"value"];
        MSGraphWorkbookTableColumn *workbookTableColumn = [[MSGraphWorkbookTableColumn alloc] initWithDictionary:[workbookTableColumnList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```