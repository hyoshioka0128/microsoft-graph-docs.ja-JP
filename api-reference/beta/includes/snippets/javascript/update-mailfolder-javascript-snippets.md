---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 86021fd7e606eab6baf025d12852367fe04e4966
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526444"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const mailFolder = {
  displayName: "displayName-value",
};

let res = await client.api('/me/mailFolders/AAMkAGVmMDEzM')
    .version('beta')
    .update({mailFolder : mailFolder});

```