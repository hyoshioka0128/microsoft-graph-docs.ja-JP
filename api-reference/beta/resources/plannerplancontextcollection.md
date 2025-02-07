---
title: プラン/プランコンテキストコレクションリソースの種類
description: plan **** は、プランがリンクされている外部コンテキストのコレクションを表します。 このリソースはオープン型であり、plan オブジェクトの一部です。 プロパティと値のペアの値は、plan プロパティのコンテキストオブジェクトです。
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 8d5394ff8a9503ab9ffba4810c9c2cad0d9a2fbf
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33344459"
---
# <a name="plannerplancontextcollection-resource-type"></a>プラン/プランコンテキストコレクションリソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]


plan **** は、プランがリンクされている外部コンテキストのコレクションを表します。 このリソースはオープン型であり、 [plan](plannerplan.md)オブジェクトの一部です。 プロパティと値のペアの値は、plan プロパティの[コンテキスト](plannerplancontext.md)オブジェクトです。


## <a name="properties"></a>プロパティ
このオープン型のプロパティを定義できます。 プロパティの値は、プロパティ名として外部コンテキストを表す特徴的識別子にする必要があります。 プロパティの値は、 [context](plannerplancontext.md)オブジェクトをプランする必要があります。 OData 要件に基づいて、オープン型のプロパティ名に次の文字を`.`含める`:`こと`%`は`@`できません:、、、。 これらの文字は、URL エンコードを使用してエンコードする必要があります。 [お気に入り] の一覧から項目を削除するには、プロパティの値`null`をに設定します。

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanContextCollection"
}-->

```json
{
  "48#19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype": {
    "@odata.type": "#microsoft.graph.plannerPlanContext",
    "associationType": "Board",
    "createdDateTime": "2015-10-14T00:57:28.4698344Z",
    "displayNameSegments": [
        "Finance Team",
        "Budget Plans"
    ],
    "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerPlanContextCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
