---
title: stringKeyObjectValuePair リソースの種類
description: キーが文字列で、値が任意の JSON オブジェクトであるキーと値のペアを表します。 これは、有効な JSON オブジェクトであるという名前の`value`プロパティがあると想定される OData オープン型です。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: b97f1f8bf10005a9e7829ee9280ebf936405b346
ms.sourcegitcommit: 121c0fad692fb3c5c01dc051481b5249e4491b48
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2019
ms.locfileid: "35620633"
---
# <a name="stringkeyobjectvaluepair-resource-type"></a>stringKeyObjectValuePair リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

キーが文字列で、値が任意の JSON オブジェクトであるキーと値のペアを表します。 これは、有効な JSON オブジェクトであるという名前の`value`プロパティがあると想定される OData オープン型です。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|Key|String|キー。|
|value|Json|任意の JSON オブジェクト。|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyObjectValuePair"
}-->

```json
{
  "key": "String",
  "value": {
    "@odata.type": "microsoft.graph.Json"
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "stringKeyObjectValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
