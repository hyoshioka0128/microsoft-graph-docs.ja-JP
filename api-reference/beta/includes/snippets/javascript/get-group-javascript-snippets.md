---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2aae756fcaa1b5602eb752703b71591eefb8c2b1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527314"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/45b7d2e7-b882-4a80-ba97-10b7a63b8fa4')
    .version('beta')
    .get();

```