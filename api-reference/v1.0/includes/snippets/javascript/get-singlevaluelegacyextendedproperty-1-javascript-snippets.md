---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a7986f271c06a4544566488c83b339b122929f92
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513141"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages/AAMkAGE1M2_bs88AACHsLqWAAA=')
    .filter('id eq 'String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color')')
    .expand('singleValueExtendedProperties($filter=id%20eq%20'String%20%7B66f5a359-4659-4830-9070-00047ec6ac6e%7D%20Name%20Color')')
    .get();

```