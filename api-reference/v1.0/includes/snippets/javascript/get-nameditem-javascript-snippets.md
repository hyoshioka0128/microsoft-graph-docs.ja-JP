---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c193c8d3db8c0b66ca0ab9bcd0fe9e8ff037b9c6
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513692"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}')
    .get();

```