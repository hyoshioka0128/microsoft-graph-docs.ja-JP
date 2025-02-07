---
title: meetingTimeSuggestion リソースの種類
description: '会議の時間、出席の可能性、個人などの情報を含む会議の提案 '
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: e5abecaf1064eee3621e8800874dc6a2c3ef9e11
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342402"
---
# <a name="meetingtimesuggestion-resource-type"></a>meetingTimeSuggestion リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

会議時間、出席の可能性、各自の空き時間情報、利用可能な会議場所を含む、会議の提案です。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingTimeSuggestion"
}-->

```json
{
  "attendeeAvailability": [{"@odata.type": "microsoft.graph.attendeeAvailability"}],
  "confidence": 1024.0,
  "locations": [{"@odata.type": "microsoft.graph.location"}],
  "meetingTimeSlot": {"@odata.type": "microsoft.graph.timeSlot"},
  "order": 1024,
  "organizerAvailability": "String",
  "suggestionReason": "String"
}

```
## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|attendeeAvailability|[attendeeAvailability](attendeeavailability.md) コレクション|この提案された会議の各出席者の空き時間情報の状態を示す配列。|
|confidence|Double|すべての出席者が出席する見込みを表すパーセンテージ。|
|locations|[location](location.md) コレクション|この提案された会議の各会議場所の名前と地理的な場所を指定する配列。|
|会議タイムスロット|[timeSlot](timeslot.md)|会議の提案されている期間。|
|降順|Int32|同じ信頼度がある場合に、chronology によって並べ替えられた、会議の時間の候補の順序 (高から低まで)。 |
|組織の空き時間情報|freeBusyStatus| この提案されている会議の開催者の空き時間情報。使用可能な値: `free`、`tentative`、`busy`、`oof`、`workingElsewhere`、`unknown`。|
|suggestionReason|String|会議時間を提案する理由。|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
