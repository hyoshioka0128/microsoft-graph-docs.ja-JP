---
title: recurrenceRange リソースの種類
description: '定期的なイベントを繰り返す期間について説明します。 '
localization_priority: Normal
ms.openlocfilehash: 4129b698e48b01e0208b88fbdc57fb777835cd4e
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32579402"
---
# <a name="recurrencerange-resource-type"></a>recurrenceRange リソースの種類

定期的な[イベント](event.md)を繰り返す期間について説明します。 

シナリオに応じて、定期的なイベントの 3 通りの期間のいずれかを指定できます。 期間の **startDate** 値は必ず指定する必要がありますが、定期的なイベントの終了は、特定の日付までに終了する、終了しない、または特定の回数繰り返した後に終了する、など指定することができます。 イベントに対して指定した期間内の定期的なイベントは、必ずこの定期的なパターンに従って発生します。 定期的なイベントは常に、[recurrencePattern](recurrencepattern.md) (イベントを繰り返す頻度)、および **recurrenceRange** (イベントを繰り返す期間) によって定義されます。

## <a name="properties"></a>プロパティ

| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|endDate|Date|定期的なパターンの適用を停止する日付。 イベントの定期的なパターンによっては、最後に会議が発生するのは、この日付にならない可能性があります。 **type** が `endDate` の場合、必要です。|
|numberOfOccurrences|Int32|イベントを繰り返す回数を指定します。 必須です。**type** が `numbered` の場合、正の値である必要があります。|
|recurrenceTimeZone|String |**startDate** プロパティと **endDate** プロパティのタイム ゾーン。 省略可能。 指定されていない場合は、イベントのタイム ゾーンが使用されます。|
|startDate|Date|定期的なパターンの適用を開始する日付。 イベントの定期的なパターンによっては、最初に会議が発生するのは、この日付以降になる場合があります。 定期的な[イベント](event.md)の **start** プロパティと同じ値である必要があります。 必須。|
|type|recurrenceRangeType|繰り返す期間。 使用可能な値: `endDate`、`noEnd`、`numbered`。 必須です。|

**type** プロパティを使用して、**recurrenceRange** のさまざまな種類から期間を指定します。 種類ごとに必要なプロパティについては、次の表の説明を参照してください。

| type プロパティ  | 繰り返す期間の種類 | 説明 | 例 | 必須のプロパティ |
|:-------|:---------------|:--------|:--------|:--------|
|`endDate` |終了日が指定された期間 | **startDate** と **endDate** の範囲内の、対応する定期的なパターンに適合するすべての日に、イベントが繰り返されます。 | 2017 年 6 月 1 日から 2017 年 6 月 15 日の期間で、イベントを繰り返します。 | **type**、**startDate**、**endDate** | 
|`noEnd`  |終了日が指定されていない期間 | **startDate** に始まる、対応する定期的なパターンに適合するすべての日に、イベントが繰り返されます。 | 2017 年 6 月 1 日に始まる期間に、イベントを無期限に繰り返します。 | **type**、**startDate** |
|`numbered`|発生回数を指定した期間 | **startDate** に始まる定期的なパターンに基づいて、**numberOfOccurrences** で指定した回数、イベントが繰り返されます。 | 2017 年 6 月 1 日に始まる期間に、イベントを 10 回繰り返します。  | **type**、**startDate**、**numberOfOccurrences** |


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recurrenceRange"
}-->

```json
{
  "endDate": "String (timestamp)",
  "numberOfOccurrences": 1024,
  "recurrenceTimeZone": "string",
  "startDate": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recurrenceRange resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
      "Warning: /api-reference/v1.0/resources/recurrencerange.md:
      Failed to parse any rows out of table with headers: | type property  | Type of recurrence range | Description | Example | Required properties |"
  ],
  "tocPath": ""
}-->
