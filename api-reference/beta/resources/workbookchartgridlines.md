---
title: workbookChartGridlines リソースの種類
description: グラフの軸の目盛線または補助目盛線を表します。
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: dce652981a16445d82b4d6e556fc7d5ce839ed26
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33348901"
---
# <a name="workbookchartgridlines-resource-type"></a>workbookChartGridlines リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

グラフの軸の目盛線または補助目盛線を表します。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[workbookChartGridlines を取得する](../api/chartgridlines-get.md) | [workbookChartGridlines](workbookchartgridlines.md) |chartGridlines オブジェクトのプロパティと関係を読み取ります。|
|[Update](../api/chartgridlines-update.md) | [workbookChartGridlines](workbookchartgridlines.md)    |ChartGridlines オブジェクトを更新します。 |

## <a name="properties"></a>プロパティ
| プロパティ     | 種類   |説明|
|:---------------|:--------|:----------|
|visible|ブール値|軸の目盛線を表示するか非表示にするかを表すブール型の値。|

## <a name="relationships"></a>関係
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|format|[workbookChartGridlinesFormat](workbookchartgridlinesformat.md)|グラフの目盛線の書式設定を表します。 読み取り専用です。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartGridlines"
}-->

```json
{
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "ChartGridlines resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
