---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 179b124b421c65dc2809f4c455e2c096a354587c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527313"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/outlook/supportedLanguages')
    .version('beta')
    .get();

```