---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/10/2017
title: Deleted
localization_priority: Normal
ms.openlocfilehash: d52ca0a9815e46ebc11a653be381ac65f3cd209e
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32574625"
---
# <a name="deleted-facet"></a>Deleted ファセット

**削除済み**リソースは、アイテムが削除されたことを示します。このバージョンの API では、リソースの値が存在する (null 以外である) ことは、ファイルが削除されたことを示します。null (または存在しない) 値は、ファイルが削除されていないことを示します。

変更の追跡と削除済みアイテムの検出の詳細については、「[アイテムの変更を表示する](../api/driveitem-delta.md)」を参照してください。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  "state"
  ],
  "@odata.type": "microsoft.graph.deleted"
}-->
```json
{
  "state": "string"
}
```
## <a name="properties"></a>プロパティ

| プロパティ | 型   | 説明                               |
|:---------|:-------|:------------------------------------------|
| state    | String | 削除されたアイテムの状態を表します。 |

## <a name="remarks"></a>注釈 

DriveItem のファセットの詳細については、「[DriveItem](driveitem.md)」を参照してください。

<!-- {
  "type": "#page.annotation",
  "description": "The deleted facet providers properties about deleted items",
  "keywords": "deleted,delete,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Deleted"
} -->
