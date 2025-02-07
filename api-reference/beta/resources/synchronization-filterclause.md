---
title: filterClause リソースの種類
description: 候補オブジェクトが満たす必要がある1つのアサーションを表し、(オブジェクト`true`がアサートを満たす) または`false` (オブジェクトはアサーションを満たしていない) のどちらかに評価されます。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 788dcd8741d89639ce2c57511ae54e466815e366
ms.sourcegitcommit: 121c0fad692fb3c5c01dc051481b5249e4491b48
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2019
ms.locfileid: "35621425"
---
# <a name="filterclause-resource-type"></a>filterClause リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

候補オブジェクトが満たす必要がある1つのアサーションを表し、(オブジェクト`true`がアサートを満たす) または`false` (オブジェクトはアサーションを満たしていない) のどちらかに評価されます。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|オペレーター名|String|ソースとターゲットのオペランドに適用される演算子の名前です。 サポートされている演算子のいずれかである必要があります。 サポートされている演算子を検出できます。|
|sourceOperandName|String|Source オペランドの名前 (テストされているオペランド)。 ソースのオペランド名は、ソースオブジェクトの属性名のいずれかと一致している必要があります。|
|targetOperand|[filterOperand](synchronization-filteroperand.md)|Source オペランドのテスト対象となる値を指定します。|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterClause"
}-->

```json
{
  "operatorName": "String",
  "sourceOperandName": "String",
  "targetOperand": {"@odata.type": "microsoft.graph.filterOperand"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "filterClause resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
