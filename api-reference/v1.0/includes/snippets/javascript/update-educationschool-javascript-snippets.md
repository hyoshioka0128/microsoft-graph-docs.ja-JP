---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6cda4e5675ced530b5e018a6ed62b6036bb16804
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514525"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const educationSchool = {
  displayName: "Fabrikam Arts High School",
  description: "Magnate school for the arts. Los Angeles School District"
};

let res = await client.api('/education/schools/{school-id}')
    .update({educationSchool : educationSchool});

```