---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 670d3ff0fac85d37581a60fc8b2a94efe4903893
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504295"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const bookingBusiness = {
  email: "admin@fabrikam.com",
  schedulingPolicy: {
      timeSlotInterval: "PT60M",
      minimumLeadTime: "P1D",
      maximumAdvance: "P30D",
      sendConfirmationsToOwner: true,
      allowStaffSelection: true
  }
};

let res = await client.api('/bookingBusinesses/fabrikam@M365B489948.onmicrosoft.com')
    .version('beta')
    .update({bookingBusiness : bookingBusiness});

```