---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d4077262008820623b6a32a277c6c4e632d6c88c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471273"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getTeamsDeviceUsageUserDetail(period='D7')')
    .get();

```