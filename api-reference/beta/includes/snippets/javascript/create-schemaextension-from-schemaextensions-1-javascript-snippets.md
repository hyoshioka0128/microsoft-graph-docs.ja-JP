---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3f09a27d01ac761ba4eba300db2f691659dcbcdf
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487250"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const schemaExtension = {
    id:"graphlearn_courses",
    description: "Graph Learn training courses extensions",
    targetTypes: [
        "Group"
    ],
    properties: [
        {
            name: "courseId",
            type: "Integer"
        },
        {
            name: "courseName",
            type: "String"
        },
        {
            name: "courseType",
            type: "String"
        }
    ]
};

let res = await client.api('/schemaExtensions')
    .version('beta')
    .post({schemaExtension : schemaExtension});

```