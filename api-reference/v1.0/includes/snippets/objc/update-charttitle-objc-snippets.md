---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: b70d4415c476ebd98a723cb35b5e0319b78dda3a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514379"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/title"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphWorkbookChartTitle *workbookChartTitle = [[MSGraphWorkbookChartTitle alloc] init];
[workbookChartTitle setOverlay: true];
[workbookChartTitle setText:@"text-value"];
[workbookChartTitle setVisible: true];

NSError *error;
NSData *workbookChartTitleData = [workbookChartTitle getSerializedDataWithError:&error];
[urlRequest setHTTPBody:workbookChartTitleData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```