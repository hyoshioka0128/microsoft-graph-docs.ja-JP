---
title: scoredEmailAddress リソースの種類
description: スコアの付いたメール アドレスを表します。
localization_priority: Normal
ms.openlocfilehash: 740173e7d5f93dc875c08508bf73100727fdf415
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32579164"
---
# <a name="scoredemailaddress-resource-type"></a>scoredEmailAddress リソースの種類

スコアの付いたメール アドレスを表します。


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|address|string|電子メール アドレス。|
|relevanceScore|double|電子メール アドレスの関連性スコア。関連性スコアは他の返された結果に関連して、並べ替えキーとして使用されます。関連性スコア値が高いほど、関連性の高い結果に対応します。関連性は、ユーザーのコミュニケーションとコラボレーション パターン、およびビジネスのリレーションシップによって決定されます。 |

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scoredEmailAddress"
}-->

```json
{
  "address": "string",
  "relevanceScore": 1024.0
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scoredEmailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
