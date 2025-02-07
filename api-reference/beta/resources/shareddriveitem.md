---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/10/2017
title: SharedDriveItem
localization_priority: Normal
ms.openlocfilehash: 3c0fa155088e39d69d52d4b14f33662d92666ed6
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33343200"
---
# <a name="shareddriveitem-resource-type"></a>SharedDriveItem リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**sharedDriveItem** リソースは、[Shares](../api/shares-get.md) API を使用して共有 [driveItem](driveitem.md) にアクセスする場合に返されます。

## <a name="json-representation"></a>JSON 表記

以下は、**sharedDriveItem** リソースの JSON 表記です。

**sharedDriveItem** リソースは [**baseItem**](baseitem.md) から派生し、そのリソースからプロパティを継承します。

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItem",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.sharedDriveItem"
}-->

```json
{
  "id": "string",
  "name": "string",
  "owner": { "@odata.type": "microsoft.graph.identitySet" },

  "driveItem": { "@odata.type": "microsoft.graph.driveItem" },
  "items": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "list": { "@odata.type": "microsoft.graph.list" },
  "listItem": { "@odata.type": "microsoft.graph.listItem" },
  "permission": { "@odata.type": "microsoft.graph.permission" },
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "site": { "@odata.type": "microsoft.graph.site" }
}
```

## <a name="properties"></a>プロパティ

| プロパティ | 型                          | 説明                                                      |
| :------- | :---------------------------- | :--------------------------------------------------------------- |
| id       | String                        | アクセスされている共有の一意識別子。              |
| name     | String                        | 共有項目の表示名。                             |
| owner    | [IdentitySet](identityset.md) | 参照されている共有アイテムの所有者に関する情報。 |

## <a name="relationships"></a>リレーションシップ

| リレーションシップ名 | 種類                | 説明
| ------------------|:--------------------|:-----------------------------------
| **driveItem**     | [**driveItem**][driveItem] | 基になる **driveItem** にアクセスするために使用
| **list**          | [**list**][list]           | 基になる **list** にアクセスするために使用
| **listItem**      | [**listItem**][listItem]   | 基になる **listItem** にアクセスするために使用
| **permission**    | [**権**][permission] | 基になる共有リンクを表す**アクセス許可**へのアクセスに使用されます。
| **site**          | [**site**][site]           | 基になる **site** にアクセスするために使用

または、個人用の OneDrive アカウントから共有される **driveItem** には、次のリレーションシップも使用できます。

| リレーションシップ名 | 種類                         | 説明
| ------------------|:-----------------------------|:-----------------------------------
| **items**         | [**driveItem**][driveItem] コレクション | 共有ルートに含まれているすべての driveItem。 このコレクションを列挙することはできません。
| **driveItem**     | [**driveItem**][driveItem]            | 基になる **driveItem** にアクセスするために使用

[driveItem]: driveitem.md
[list]: list.md
[listItem]: listitem.md
[permission]: permission.md
[site]: site.md

## <a name="methods"></a>メソッド

| Method                                  | REST パス                |
| :-------------------------------------- | :----------------------- |
| [共有アイテムを取得する](../api/shares-get.md) | `GET /shares/{share-id}` |

## <a name="remarks"></a>備考

DriveItem のファセットの詳細については、「[DriveItem](driveitem.md)」を参照してください。

<!--
{
  "type": "#page.annotation",
  "description": "Share resource returns information about a shared item or collection of items.",
  "keywords": "share,shared,sharing root,shared files, shared items",
  "section": "documentation",
  "tocPath": "Resources/Share",
  "suppressions": []
}
-->
