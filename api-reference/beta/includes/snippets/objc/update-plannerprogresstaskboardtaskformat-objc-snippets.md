---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: cefbad14e16c68bc4c5a62b4e340d576b9ea29d5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485084"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/planner/tasks/'id'/progressTaskBoardFormat"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"" forHTTPHeaderField:@"If-Match"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphPlannerProgressTaskBoardTaskFormat *plannerProgressTaskBoardTaskFormat = [[MSGraphPlannerProgressTaskBoardTaskFormat alloc] init];
[plannerProgressTaskBoardTaskFormat setOrderHint:@"A6673H Ejkl!"];

NSError *error;
NSData *plannerProgressTaskBoardTaskFormatData = [plannerProgressTaskBoardTaskFormat getSerializedDataWithError:&error];
[urlRequest setHTTPBody:plannerProgressTaskBoardTaskFormatData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```