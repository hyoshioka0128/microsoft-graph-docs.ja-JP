---
title: daylightTimeZoneOffset リソースの種類
description: タイム ゾーンが標準時から夏時間に切り替わるタイミングを指定します。
localization_priority: Normal
ms.openlocfilehash: b6e965a154b0219a78898c2bf021cac2bb11c238
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33340965"
---
# <a name="daylighttimezoneoffset-resource-type"></a>daylightTimeZoneOffset リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

タイム ゾーンが標準時から夏時間に切り替わるタイミングを指定します。

たとえば、タイム ゾーンに次のプロパティが指定されているとします。

- **bias**: 300
- **daylightBias**: -100
- **dayOccurrence**: 4
- **dayOfWeek**: "日曜日"
- **month**: 5
- **time** は 02:00:00 で、_ **year** は 0 です。つまり、夏時間の間は、時刻が UTC より +300-100=200 分進んでいることを意味します。 夏時間から標準時への切り替えは、毎年 5 月の第 4 日曜日の午前 2 時に行われます。


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| daylightBias | Edm.Int32 | 夏時間の協定世界時 (UTC) からの時間オフセットです。 この値は分単位です。  |
| dayOccurrence | Edm.Int32 | 標準時から夏時間への切り替えが月の何番目の曜日に行われるかを表します。 |
| dayOfWeek | string | 標準時から夏時間への切り替えが行われる曜日を表します。 |
| month | Edm.Int32 | 標準時から夏時間への切り替えが行われる月を表します。 |
| time | Edm.TimeOfDay | 標準時から夏時間への切り替えが行われる時刻を表します。 |
| year | Edm.Int32 | 標準時から夏時間への切り替えが年に何回行われるかを表します。 たとえば、値 0 は年に 1 回を意味します。|


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.daylightTimeZoneOffset"
}-->

```json
{
  "daylightBias": "Int32",
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
  "description": "daylightTimeZoneOffset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
