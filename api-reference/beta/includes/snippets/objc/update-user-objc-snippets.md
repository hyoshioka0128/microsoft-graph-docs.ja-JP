---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5a23d3c38d6cd0b287c2ae1f746dc903bfaff113
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526874"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphUser *user = [[MSGraphUser alloc] init];
[user setAccountEnabled: true];
NSMutableArray *assignedLicensesList = [[NSMutableArray alloc] init];
MSGraphAssignedLicense *assignedLicenses = [[MSGraphAssignedLicense alloc] init];
NSMutableArray *disabledPlansList = [[NSMutableArray alloc] init];
[disabledPlansList addObject: @"bea13e0c-3828-4daa-a392-28af7ff61a0f"];
[assignedLicenses setDisabledPlans:disabledPlansList];
[assignedLicenses setSkuId:@"skuId-value"];
[assignedLicensesList addObject: assignedLicenses];
[user setAssignedLicenses:assignedLicensesList];
NSMutableArray *assignedPlansList = [[NSMutableArray alloc] init];
MSGraphAssignedPlan *assignedPlans = [[MSGraphAssignedPlan alloc] init];
[assignedPlans setAssignedDateTime: "2016-10-19T10:37:00Z"];
[assignedPlans setCapabilityStatus:@"capabilityStatus-value"];
[assignedPlans setService:@"service-value"];
[assignedPlans setServicePlanId:@"bea13e0c-3828-4daa-a392-28af7ff61a0f"];
[assignedPlansList addObject: assignedPlans];
[user setAssignedPlans:assignedPlansList];
NSMutableArray *businessPhonesList = [[NSMutableArray alloc] init];
[businessPhonesList addObject: @"businessPhones-value"];
[user setBusinessPhones:businessPhonesList];
[user setCity:@"city-value"];

NSError *error;
NSData *userData = [user getSerializedDataWithError:&error];
[urlRequest setHTTPBody:userData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```