---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/10/2017
title: SharePointIds
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 01e4c3087f9504255975ab28f935ceed8815b6b0
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33343100"
---
# <a name="sharepointids-resource-type"></a>SharePointIds リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**SharePointIds** リソースは、SharePoint サイトまたは OneDrive for Business に保存されているアイテムのさまざまな識別子を 1 つの構造にグループ化します。

**注:** 個人用の OneDrive から返されたアイテムには **SharePointIds** ファセットは含まれません。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "listId", "listItemId", "listItemUniqueId", "siteId", "siteUrl", "webId" ],
  "@odata.type": "microsoft.graph.sharepointIds"
}-->

```json
{
    "listId": "string",
    "listItemId": "string",
    "listItemUniqueId": "string",
    "siteId": "string",
    "siteUrl": "url",
    "tenantId": "string",
    "webId": "string"
}
```

## <a name="properties"></a>プロパティ

| プロパティ         | 型         | 説明
|:-----------------|:-------------|:-------------------------------------------
| listId           | string       | SharePoint 内にあるアイテムの一覧の一意識別子 (guid)。
| listItemId       | string       | 含まれているリスト内にあるアイテムの整数の識別子。
| listItemUniqueId | string       | OneDrive for Business または SharePoint サイト内のアイテムの一意識別子 (guid)。
| siteId           | string       | アイテムのサイト コレクション (SPSite) の一意識別子 (guid)。
| siteUrl          | string (URL) | アイテムが含まれるサイトの SharePoint URL です。
| tenantId         | string       | テナントの一意識別子 (guid)。
| webId            | string       | アイテムのサイト (SPWeb) の一意識別子 (guid)。

## <a name="remarks"></a>備考

**driveItem** のファセットに関する詳細については、「[**driveItem**](driveitem.md)」を参照してください。



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "The SharepointIds facet provides Sharepoint ids associated with an item.",
  "keywords": "item, unique, id, csom, facet",
  "section": "documentation",
  "tocPath": "Facets/SharepointIds",
  "suppressions": []
}
-->
