---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/11/2017
title: List
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 5e078c79603235059cbe326c850e51dfa33d2f8e
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345338"
---
# <a name="list-resource"></a>List リソース

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**list** リソースは [site][] 内のリストを表します。
このリソースには、テンプレートとフィールドの定義を含め、リストの最上位レベルのプロパティが含まれています。

## <a name="tasks-on-a-list"></a>リスト上のタスク

list リソースで使用可能なタスクを次に示します。
**注:** このベータ版では、リスト上の移動だけが可能であり、リストの作成や更新はできません。
ただし、[リスト アイテム]の [listItem] の作成または更新は可能です。

以下のすべての例は、`https://graph.microsoft.com/beta/sites/{site-id}` などのサイトからの相対指定です。

| 共通タスク               | HTTP メソッド
|:--------------------------|:------------------------------
| [リストを取得する][]              | GET /lists/{list-id}
| [リスト アイテムを列挙する][]  | GET /lists/{list-id}/items
| [リスト アイテムを更新する][]      | PATCH /lists/{list-id}/items/{item-id}
| [リスト アイテムを削除する][]      | DELETE /lists/{list-id}/items/{item-id}
| [リスト アイテムを作成する][]      | POST /lists/{list-id}
| [最近のアクティビティを取得する][] | GET /lists/{list-id}/activities

[リストを取得する]: ../api/list-get.md
[リスト アイテムを列挙する]: ../api/listitem-list.md
[リスト アイテムを更新する]: ../api/listitem-update.md
[リスト アイテムを削除する]: ../api/listitem-delete.md
[リスト アイテムを作成する]: ../api/listitem-create.md
[最近のアクティビティを取得する]: ../api/activities-list.md

## <a name="json-representation"></a>JSON 表記

以下は、**list** リソースの JSON 表記です。

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.list",
       "keyProperty": "id", 
       "optionalProperties": [ "items", "drive"] } -->

```json
{
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "displayName": "title of list",
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "items": [ { "@odata.type": "microsoft.graph.listItem" } ],
  "list": {
    "@odata.type": "microsoft.graph.listInfo",
    "hidden": false,
    "template": "documentLibrary | genericList | survey | links | announcements | contacts ..."
  },
  "system": false,

  /* inherited from baseItem */
  "id": "string",
  "name": "name of list",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "description": "description of list",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "webUrl": "url to visit the list in a browser"
}
```

## <a name="properties"></a>プロパティ

**list** リソースには以下のプロパティがあります。

| プロパティ名    | 種類                             | 説明
|:-----------------|:---------------------------------|:---------------------------
| **columns**      | Collection([columnDefinition][]) | このリストのフィールド定義のコレクションです。
| **contentTypes** | Collection([contentType][])      | このリスト内に存在するコンテンツ タイプのコレクションです。
| **displayName**  | string                           | リストの表示可能なタイトルです。
| **list**         | [listInfo][]                     | リストに関する追加の詳細を示します。
| **system**       | [systemFacet][]                  | 存在する場合は、これがシステム管理のリストであることを示しています。 読み取り専用です。

次のプロパティは、**[baseItem][]** から継承しています。

| プロパティ名            | 種類             | 説明
|:-------------------------|:-----------------|:-------------------------------
| **id**                   | string           | アイテムの一意識別子。読み取り専用です。
| **name**                 | string           | アイテムの名前。
| **createdBy**            | [identitySet][]  | このアイテムの作成者の ID です。 読み取り専用です。
| **createdDateTime**      | DateTimeOffset   | アイテムが作成された日時。読み取り専用です。
| **説明**          | string           | アイテムの説明テキストです。
| **lastModifiedBy**       | [identitySet][]  | このアイテムの最終変更者の ID です。 読み取り専用です。
| **lastModifiedDateTime** | DateTimeOffset   | アイテムが最後に変更された日時。読み取り専用です。
| **webUrl**               | string (URL)     | ブラウザーでアイテムを表示する URL。読み取り専用です。

## <a name="relationships"></a>リレーションシップ

**list** リソースには、他のリソースと次のような関係があります。

| リレーションシップ名 | 種類                        | 説明
|:------------------|:----------------------------|:------------------------------
| **activities**    | [itemActivity][] コレクション | このリスト内で行われた最近のアクティビティです。
| **ドライブ**         | [drive][]                   | ドキュメント ライブラリにのみ存在します。 [driveItems][driveItem] を含む [drive][] リソースとしてリストにアクセスできます。
| **items**         | Collection([listItem][])    | リストに含まれているすべてのアイテム。

[baseItem]: baseitem.md
[contentType]: contenttype.md
[drive]: drive.md
[driveItem]: driveitem.md
[columnDefinition]: columndefinition.md
[identitySet]: identityset.md
[itemActivity]: itemactivity.md
[listInfo]: listinfo.md
[listItem]: listitem.md
[サイト]: site.md
[systemFacet]: systemfacet.md

<!--
{
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/Lists",
  "tocBookmarks": {
    "Lists": "#"
  },
  "suppressions": []
}
-->
