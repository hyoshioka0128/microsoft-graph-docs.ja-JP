---
title: workbookRangeView リソースの種類
description: RangeView は、親の範囲の表示されているセルのセットを表します。
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: fdc09b4c88e3105624f322697784cfa4e654ee96
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345828"
---
# <a name="workbookrangeview-resource-type"></a>workbookRangeView リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

RangeView は、親の範囲の表示されているセルのセットを表します。

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[行を一覧表示する](../api/workbookrangeview-list-rows.md) |[workbookRangeView](workbookrangeview.md) コレクション| workbookRangeView オブジェクト コレクションを取得します。|
|[Itemat](../api/workbookrangeview-itemat.md)|[workbookRangeView](workbookrangeview.md)|インデックスに基づいて範囲ビューの項目を取得します。|
|[Range](../api/workbookrangeview-range.md)|[workbookRange](workbookrange.md)|範囲ビューに関連付けられた範囲オブジェクトを返します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|columnCount|Int32|表示されている列の数を返します。読み取り専用。|
|formulas|Json|A1 スタイル表記の数式を表します。 |
|formulasLocal|Json|ユーザーの言語と数値書式ロケールで、A1 スタイル表記の数式を表します。たとえば、英語の数式 "=SUM(A1, 1.5)" は、ドイツ語では "=SUMME(A1; 1,5)" になります。    |
|formulasR1C1|Json|R1C1 スタイル表記の数式を表します。   |
|index|Int32|範囲のインデックス。|
|numberFormat|Json|指定したセルの Excel の数値書式コードを表します。読み取り専用です。 |
|rowCount|Int32|表示されている行の数を返します。読み取り専用。  |
|text|Json|指定した範囲のテキスト値。テキスト値は、セルの幅には依存しません。Excel UI で発生する # 記号による置換は、この API から返されるテキスト値には影響しません。読み取り専用です。    |
|valueTypes|Json|各セルのデータの種類を表します。読み取り専用です。使用可能な値は次のとおりです。Unknown、Empty、String、Integer、Double、Boolean、Error。 |
|values|Json|指定した範囲ビューの Raw 値を表します。返されるデータの型は、文字列、数値、ブール値のいずれかになります。エラーが含まれているセルは、エラー文字列を返します。   |

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|rows|[workbookRangeView](workbookrangeview.md) コレクション| 範囲に関連付けられている範囲ビューのコレクションを表します。読み取り専用です。  読み取り専用です。|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeView"
}-->
```json
{
  "cellAddresses": "Json",
  "columnCount": 1024,
  "formulas": "Json",
  "formulasLocal": "Json",
  "formulasR1C1": "Json",
  "id": "String (identifier)",
  "index": 1024,
  "numberFormat": "Json",
  "rowCount": 1024,
  "text": "Json",
  "valueTypes": "Json",
  "values": "Json"
}
```
