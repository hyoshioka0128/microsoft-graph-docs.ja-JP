---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3aaccb429b08949cd056fb883d6d7bf051692d07
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34469784"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/format/borders')
    .get();

```