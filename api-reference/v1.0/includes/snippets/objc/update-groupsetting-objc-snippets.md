---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fcda91aedc09076bff488587636200e13aec40ca
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513966"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/groupSettings/{id}"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphGroupSetting *groupSetting = [[MSGraphGroupSetting alloc] init];
[groupSetting setDisplayName:@"displayName-value"];
[groupSetting setTemplateId:@"templateId-value"];
NSMutableArray *valuesList = [[NSMutableArray alloc] init];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"CustomBlockedWordsList"];
[values setValue:@""];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"EnableMSStandardBlockedWords"];
[values setValue:@"False"];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"ClassificationDescriptions"];
[values setValue:@""];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"DefaultClassification"];
[values setValue:@""];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"PrefixSuffixNamingRequirement"];
[values setValue:@""];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"AllowGuestsToBeGroupOwner"];
[values setValue:@"False"];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"AllowGuestsToAccessGroups"];
[values setValue:@"True"];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"GuestUsageGuidelinesUrl"];
[values setValue:@""];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"GroupCreationAllowedGroupId"];
[values setValue:@"62e90394-69f5-4237-9190-012177145e10"];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"AllowToAddGuests"];
[values setValue:@"True"];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"UsageGuidelinesUrl"];
[values setValue:@""];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"ClassificationList"];
[values setValue:@""];
[valuesList addObject: values];
MSGraphSettingValue *values = [[MSGraphSettingValue alloc] init];
[values setName:@"EnableGroupCreation"];
[values setValue:@"True"];
[valuesList addObject: values];
[groupSetting setValues:valuesList];

NSError *error;
NSData *groupSettingData = [groupSetting getSerializedDataWithError:&error];
[urlRequest setHTTPBody:groupSettingData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```