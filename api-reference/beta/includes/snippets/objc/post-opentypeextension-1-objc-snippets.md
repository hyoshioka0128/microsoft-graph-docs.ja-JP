---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 037f7485ec63ba4546a5d42d075636d8a7207e2e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526197"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/messages"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphMessage *message = [[MSGraphMessage alloc] init];
[message setSubject:@"Annual review"];
MSGraphItemBody *body = [[MSGraphItemBody alloc] init];
[body setContentType: [MSGraphBodyType html]];
[body setContent:@"You should be proud!"];
[message setBody:body];
NSMutableArray *toRecipientsList = [[NSMutableArray alloc] init];
MSGraphRecipient *toRecipients = [[MSGraphRecipient alloc] init];
MSGraphEmailAddress *emailAddress = [[MSGraphEmailAddress alloc] init];
[emailAddress setAddress:@"rufus@contoso.com"];
[toRecipients setEmailAddress:emailAddress];
[toRecipientsList addObject: toRecipients];
[message setToRecipients:toRecipientsList];
NSMutableArray *extensionsList = [[NSMutableArray alloc] init];
MSGraphExtension *extensions = [[MSGraphExtension alloc] init];
[extensions setExtensionName:@"Com.Contoso.Referral"];
[extensions setCompanyName:@"Wingtip Toys"];
[extensions setExpirationDate: "2015-12-30T11:00:00Z"];
[extensions setDealValue: 10000];
[extensionsList addObject: extensions];
[message setExtensions:extensionsList];

NSError *error;
NSData *messageData = [message getSerializedDataWithError:&error];
[urlRequest setHTTPBody:messageData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```