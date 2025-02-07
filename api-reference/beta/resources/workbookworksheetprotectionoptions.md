---
title: workbookWorksheetProtectionOptions リソースの種類
description: シート保護のオプションを表します。
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: c5f5a953490eebf456ce4cc37b515c758630b3ce
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33348860"
---
# <a name="workbookworksheetprotectionoptions-resource-type"></a>workbookWorksheetProtectionOptions リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

シート保護のオプションを表します。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|allowAutoFilter|boolean|自動フィルター機能の使用を可能にするワークシート保護オプションを表します。|
|allowDeleteColumns|boolean|列の削除を可能にするワークシート保護オプションを表します。|
|allowDeleteRows|boolean|行の削除を可能にするワークシート保護オプションを表します。|
|allowFormatCells|boolean|セルの書式設定を可能にするワークシート保護オプションを表します。|
|allowFormatColumns|boolean|列の書式設定を可能にするワークシート保護オプションを表します。|
|allowFormatRows|boolean|行の書式設定を可能にするワークシート保護オプションを表します。|
|allowInsertColumns|boolean|列の挿入を可能にするワークシート保護オプションを表します。|
|allowInsertHyperlinks|boolean|ハイパーリンクの挿入を可能にするワークシート保護オプションを表します。|
|allowInsertRows|boolean|行の挿入を可能にするワークシート保護オプションを表します。|
|allowPivotTables|boolean|ピボット テーブル機能の使用を可能にするワークシート保護オプションを表します。|
|allowSort|ブール値|並ベ替え機能の使用を可能にするワークシート保護オプションを表します。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookWorksheetProtectionOptions"
}-->

```json
{
  "allowAutoFilter": true,
  "allowDeleteColumns": true,
  "allowDeleteRows": true,
  "allowFormatCells": true,
  "allowFormatColumns": true,
  "allowFormatRows": true,
  "allowInsertColumns": true,
  "allowInsertHyperlinks": true,
  "allowInsertRows": true,
  "allowPivotTables": true,
  "allowSort": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "workbookWorksheetProtectionOptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
