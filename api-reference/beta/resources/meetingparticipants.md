---
title: 会議参加者リソースの種類
description: 会議の参加者。
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: f6446ec0b896854e2566d4de82acfdb53bee893d
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342409"
---
# <a name="meetingparticipants-resource-type"></a>会議参加者リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

会議の参加者。

## <a name="properties"></a>プロパティ

| プロパティ       | 型    | 説明|
|:---------------|:--------|:----------|
| attendees | [meetingParticipantInfo](meetingparticipantinfo.md)コレクション |  |
| organizer | [meetingParticipantInfo](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipants"
}-->
```json
{
  "attendees": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
  "organizer": {"@odata.type": "#microsoft.graph.meetingParticipantInfo"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingParticipants resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
