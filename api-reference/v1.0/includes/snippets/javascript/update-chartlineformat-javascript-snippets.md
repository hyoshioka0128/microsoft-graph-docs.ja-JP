---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: cfb0d39e4deb7b97c75d703ab70fe71ef1cc6c36
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495763"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookChartLineFormat = {
  color: "color-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/line')
    .update({workbookChartLineFormat : workbookChartLineFormat});

```