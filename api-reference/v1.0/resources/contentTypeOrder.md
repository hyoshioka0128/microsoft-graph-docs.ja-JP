---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
localization_priority: Normal
ms.openlocfilehash: ccea5804c3f4eddb02b5d4163302362f29b5fbc8
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32561328"
---
# <a name="contenttypeorder-resource-type"></a>ContentTypeOrder リソースの種類

**contentTypeOrder** リソースは、コンテンツ タイプが選択 UI に表示される順序を指定します。

## <a name="json-representation"></a>JSON 表記

以下は、**contentTypeOrder** リソースの JSON 表記です。
<!-- { "blockType": "resource", "@type": "microsoft.graph.contentTypeOrder", "@type.aka": "oneDrive.contentTypeOrderFacet" } -->

```json
{
  "default": true,
  "position": 2
}
```

## <a name="properties"></a>プロパティ

| プロパティ名 | 種類    | 説明
|:--------------|:--------|:----------------------------------------------------
| **default**   | boolean | 既定のコンテンツ タイプかどうか。
| **position**  | Int32   | コンテンツ タイプが選択 UI で表示される位置を指定します。

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeOrder"
} -->
