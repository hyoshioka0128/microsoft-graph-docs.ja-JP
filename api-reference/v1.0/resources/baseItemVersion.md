---
title: BaseItemVersion リソースの種類
description: '**baseItemVersion** リソースは、アイテムまたはエンティティの旧バージョンを表します。'
localization_priority: Normal
ms.openlocfilehash: bd28f9c8dc5be2bc6422aca2eb756aba78b8e393
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32569439"
---
# <a name="baseitemversion-resource-type"></a>BaseItemVersion リソースの種類

**baseItemVersion** リソースは、アイテムまたはエンティティの旧バージョンを表します。


## <a name="json-representation"></a>JSON 表記

<!--{
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.baseItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a>プロパティ

|      プロパティ名       |                         種類                         |                               説明                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| **id**                   | string                                               | バージョンの ID。 読み取り専用。                                       |
| **lastModifiedBy**       | [IdentitySet](../resources/identityset.md)           | 最後にバージョンを変更したユーザーの ID。 読み取り専用です。        |
| **lastModifiedDateTime** | [DateTimeOffset](../resources/timestamp.md)          | バージョンが最後に変更された日時。 読み取り専用。                 |
| **publication**          | [PublicationFacet](../resources/publicationfacet.md) | 特定のバージョンのパブリケーション ステータスを示します。 読み取り専用です。 |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
