---
title: mailboxSettings リソースの種類
description: サインイン ユーザーのプライマリ メールボックスの設定。
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: bf5ca7b6e9a653946f5ea1ff0a302c8499f2e02d
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345126"
---
# <a name="mailboxsettings-resource-type"></a>mailboxSettings リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

サインイン ユーザーのプライマリ メールボックスの設定。


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|archiveFolder|string|ユーザーのアーカイブ フォルダーのフォルダー ID。|
|automaticRepliesSetting|[automaticRepliesSetting](automaticrepliessetting.md)|サインイン ユーザーからのメッセージを使用して、着信メールの送信者に自動的に通知する構成設定。|
|language|[localeInfo](localeinfo.md)|優先言語および国/地域を含むユーザーのロケール情報。|
|timeZone|string|ユーザーのメールボックスの既定のタイム ゾーン。|
|workingHours|[workingHours](workinghours.md)|ユーザーが働く曜日と、特定のタイムゾーンの時間。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "archiveFolder"
  ],
  "@odata.type": "microsoft.graph.mailboxSettings"
}-->

```json
{
  "archiveFolder": "string",
  "automaticRepliesSetting": {"@odata.type": "microsoft.graph.automaticRepliesSetting"},
  "language": {"@odata.type": "microsoft.graph.localeInfo"},
  "timeZone": "string",
  "workingHours": {"@odata.type": "microsoft.graph.workingHours"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "mailboxSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
