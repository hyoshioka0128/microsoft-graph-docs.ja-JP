---
title: ChartSeries リソースの種類
description: グラフのデータ系列を表します。
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: b9a857f127848f1ed0da8de673902527e3858ffe
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32569040"
---
# <a name="chartseries-resource-type"></a>ChartSeries リソースの種類

グラフのデータ系列を表します。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Get ChartSeries](../api/chartseries-get.md) | [WorkbookChartSeries](chartseries.md) |chartSeries オブジェクトのプロパティと関係を読み取ります。|
|[ChartPoints を作成する](../api/chartseries-post-points.md) |[ChartPoints](chartpoint.md)| ポイント コレクションに投稿して、新しい ChartPoints を作成します。|
|[ポイントを一覧表示する](../api/chartseries-list-points.md) |[ChartPoints](chartpoint.md) コレクション| ChartPoints オブジェクトのコレクションを取得します。|
|[Update](../api/chartseries-update.md) | [WorkbookChartSeries](chartseries.md) |ChartSeries オブジェクトを更新します。 |
|[List](../api/chartseries-list.md) | [WorkbookChartSeries](chartseries.md)コレクション |chartSeries オブジェクトのコレクションを取得します。 |
|[ItemAt](../api/chartseriescollection-itemat.md)|[WorkbookChartSeries](chartseries.md)|コレクション内の位置に基づいてデータ系列を取得します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|name|string|グラフのデータ系列の名前を表します。|

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|format|[WorkbookChartSeriesFormat](chartseriesformat.md)|グラフ の系列の書式設定を表します。これには塗りつぶしと線の書式設定などがあります。値の取得のみ可能です。|
|points|[WorkbookChartPoint](chartpoint.md)コレクション|データ系列にあるすべてのポイントのコレクションを返します。 値の取得のみ可能です。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartSeries"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeries resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
