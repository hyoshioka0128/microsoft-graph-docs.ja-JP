---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d9673b2deebd39424eab9f97f0adaef176bb242e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495545"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *workbookChartPointList = [[NSMutableArray alloc] init];
        workbookChartPointList = [jsonFinal valueForKey:@"value"];
        MSGraphWorkbookChartPoint *workbookChartPoint = [[MSGraphWorkbookChartPoint alloc] initWithDictionary:[workbookChartPointList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```