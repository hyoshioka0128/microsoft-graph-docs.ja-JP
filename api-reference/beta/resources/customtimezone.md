---
title: customTimeZone リソースの種類
description: 標準時から夏時間またはその逆への切り替えが標準となっていないタイム ゾーンを表します。
localization_priority: Normal
ms.openlocfilehash: 7882a19087c22ed88dc67e3f3b876af41c9a222e
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33341017"
---
# <a name="customtimezone-resource-type"></a>customTimeZone リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

標準時から夏時間またはその逆への切り替えが標準となっていないタイム ゾーンを表します。


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| bias | Edm.Int32 | タイム ゾーンの協定世界時 (UTC) からの時間オフセットです。 この値は分単位です。UTC より時間が進んでいるタイム　ゾーンには正のオフセット、UTC より時間が遅れているタイム ゾーンには負のオフセットを設定します。|
| daylightOffset | [daylightTimeZoneOffset](daylighttimezoneoffset.md) | タイム ゾーンが標準時から夏時間に切り替わるタイミングを指定します。 |
| name | string | カスタム タイム ゾーンの名前。 |
| standardOffset | [standardTimeZoneOffset](standardtimezoneoffset.md) | タイム ゾーンが夏時間から標準時に切り替わるタイミングを指定します。 |


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.customTimeZone"
}-->

```json
{
  "bias": "Int32",
  "daylightOffset": {"@odata.type": "microsoft.graph.daylightTimeZoneOffset"},
  "name": "string",
  "standardOffset": {"@odata.type": "microsoft.graph.standardTimeZoneOffset"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "customTimeZone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
