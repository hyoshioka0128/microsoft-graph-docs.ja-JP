---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2a1ce0cce64b3edc383edcc226550ffa9973cdc7
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527056"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/security/tiIndicators/submitTiIndicators"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

NSMutableDictionary *payloadDictionary = [[NSMutableDictionary alloc] init];

NSMutableArray *valueList = [[NSMutableArray alloc] init];
MSGraphTiIndicator *value = [[MSGraphTiIndicator alloc] init];
NSMutableArray *activityGroupNamesList = [[NSMutableArray alloc] init];
[value setActivityGroupNames:activityGroupNamesList];
[value setConfidence: 0];
[value setDescription:@"This is a canary indicator for demo purpose. Take no action on any observables set in this indicator."];
[value setExpirationDateTime: "2019-03-02T00:44:03.1668987+03:00"];
[value setExternalId:@"Test--8586509942423126760MS164-0"];
[value setFileHashType: [MSGraphFileHashType sha256]];
[value setFileHashValue:@"b555c45c5b1b01304217e72118d6ca1b14b7013644a078273cea27bbdc1cf9d6"];
NSMutableArray *killChainList = [[NSMutableArray alloc] init];
[value setKillChain:killChainList];
NSMutableArray *malwareFamilyNamesList = [[NSMutableArray alloc] init];
[value setMalwareFamilyNames:malwareFamilyNamesList];
[value setSeverity: 0];
NSMutableArray *tagsList = [[NSMutableArray alloc] init];
[value setTags:tagsList];
[value setTargetProduct:@"Azure Sentinel"];
[value setThreatType:@"WatchList"];
[value setTlpLevel: [MSGraphTlpLevel green]];
[valueList addObject: value];
MSGraphTiIndicator *value = [[MSGraphTiIndicator alloc] init];
NSMutableArray *activityGroupNamesList = [[NSMutableArray alloc] init];
[value setActivityGroupNames:activityGroupNamesList];
[value setConfidence: 0];
[value setDescription:@"This is a canary indicator for demo purpose. Take no action on any observables set in this indicator."];
[value setExpirationDateTime: "2019-03-02T00:44:03.1748779+03:00"];
[value setExternalId:@"Test--8586509942423126760MS164-1"];
[value setFileHashType: [MSGraphFileHashType sha256]];
[value setFileHashValue:@"1796b433950990b28d6a22456c9d2b58ced1bdfcdf5f16f7e39d6b9bdca4213b"];
NSMutableArray *killChainList = [[NSMutableArray alloc] init];
[value setKillChain:killChainList];
NSMutableArray *malwareFamilyNamesList = [[NSMutableArray alloc] init];
[value setMalwareFamilyNames:malwareFamilyNamesList];
[value setSeverity: 0];
NSMutableArray *tagsList = [[NSMutableArray alloc] init];
[value setTags:tagsList];
[value setTargetProduct:@"Azure Sentinel"];
[value setThreatType:@"WatchList"];
[value setTlpLevel: [MSGraphTlpLevel green]];
[valueList addObject: value];
payloadDictionary[@"value"] = valueList;

NSData *data = [NSJSONSerialization dataWithJSONObject:payloadDictionary options:kNilOptions error:&error];
[urlRequest setHTTPBody:data];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```