---
title: standardTimeZoneOffset リソースの種類
description: タイム ゾーンが夏時間から標準時に切り替わるタイミングを指定します。
localization_priority: Normal
ms.openlocfilehash: fb6327c49c51e9bdee7e2ac5941257a45092fbb8
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345732"
---
# <a name="standardtimezoneoffset-resource-type"></a>standardTimeZoneOffset リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

タイム ゾーンが夏時間から標準時に切り替わるタイミングを指定します。

たとえば、タイム ゾーンに次のプロパティが指定されているとします。

- **dayOccurrence**: 3
- **dayOfWeek**: "日曜日"
- **month**: 10
- **time** は 02:00:00 で、_ **year** は 0 です。つまり、夏時間から標準時への切り替えは、毎年 10 月の第 3 日曜日の午前 2 時に行われることを意味します。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| dayOccurrence | Edm.Int32 | 夏時間から標準時への切り替えが月の何番目の曜日に行われるかを表します。 |
| dayOfWeek | string | 夏時間から標準時への切り替えが行われる曜日を表します。 |
| month | Edm.Int32 | 夏時間から標準時への切り替えが行われる月を表します。 |
| time | Edm.TimeOfDay | 夏時間から標準時への切り替えが行われる時刻を表します。 |
| year | Edm.Int32 | 夏時間から標準時への切り替えが年に何回行われるかを表します。 たとえば、値 0 は年に 1 回を意味します。|


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.standardTimeZoneOffset"
}-->

```json
{
  "dayOccurrence": "Int32",
  "dayOfWeek": "string",
  "month": "Int32",
  "time": "TimeOfDay",
  "year": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "standardTimeZoneOffset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
