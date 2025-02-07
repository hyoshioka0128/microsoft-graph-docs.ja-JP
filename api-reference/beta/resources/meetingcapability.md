---
title: 会議機能リソースの種類
description: 会議の機能が含まれています。
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 55a577490ee4c40bbd4adcc63a7e4aa7f38c8dd1
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342599"
---
# <a name="meetingcapability-resource-type"></a>会議機能リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

会議の機能が含まれています。

## <a name="properties"></a>プロパティ

| プロパティ                          | 型    | 説明                                                        |
|:----------------------------------|:--------|:-------------------------------------------------------------------|
| allowAnonymousUsersToDialOut      | Boolean | 匿名ユーザーが会議でダイヤルアウトが許可されているかどうかを示します。 |
| allowAnonymousUsersToStartMeeting | Boolean | 匿名ユーザーが会議の開始を許可されているかどうかを示します。  |
| autoAdmittedUsers                 | String  | 使用可能な値は、`everyoneInCompany`、`everyone` です。              |

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingCapability"
}-->
```json
{
  "allowAnonymousUsersToDialOut": true,
  "allowAnonymousUsersToStartMeeting": true,
  "autoAdmittedUsers": "everyoneInCompany | everyone"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingCapability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
