---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a568589035eb1ebcf02c2201682239ca2ddcc29b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485138"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/names/{name}/range/format/protection"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphWorkbookFormatProtection *workbookFormatProtection = [[MSGraphWorkbookFormatProtection alloc] init];
[workbookFormatProtection setLocked: true];
[workbookFormatProtection setFormulaHidden: true];

NSError *error;
NSData *workbookFormatProtectionData = [workbookFormatProtection getSerializedDataWithError:&error];
[urlRequest setHTTPBody:workbookFormatProtectionData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```