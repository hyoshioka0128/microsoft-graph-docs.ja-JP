---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: be7e866a264db8ef7e30677ec9969cfe902aef3e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514507"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/root/workbook/worksheets/{id}/range/columnsBefore(count=2)')
    .post();

```