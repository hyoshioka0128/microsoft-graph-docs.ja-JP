---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 76a1d2c781cdc3d20f1f34c3d5f512f21c5b8c10
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514528"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const educationClass = {
  description: "History - World History 1",
  displayName: "World History Level 1",
};

let res = await client.api('/education/classes/{class-id}')
    .update({educationClass : educationClass});

```