---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 00f958fa57b6026ab08673861671ea2899cdde13
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464581"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const message = {
    subject: "Party planning",
    toRecipients:[
      {
          emailAddress:{
              name:"Samantha Booth",
              address:"samanthab@contoso.onmicrosoft.com"
          }
      }
    ],
    mentions:[
      {    
        mentioned:{
          name:"Dana Swope",
          address:"danas@contoso.onmicrosoft.com"
         }
      }
    ]
};

let res = await client.api('/me/messages')
    .version('beta')
    .post({message : message});

```