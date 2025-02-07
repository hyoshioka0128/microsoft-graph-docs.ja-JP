---
title: program リソースの種類
description: 'Azure AD access のレビュー機能であるプログラムは、プログラムコントロールを保持するコンテナーです。 テナントには、1つ以上のプログラムを含めることができます。  各コントロールは、アクセスレビューをプログラムにリンクして、関連するアクセスレビューを簡単に見つけられるようにします。  '
localization_priority: Normal
ms.openlocfilehash: 7c0016cb194acd7ad8533acb34650b57df720ace
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33344030"
---
# <a name="program-resource-type"></a>program リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Azure AD access の[レビュー](accessreviews-root.md)機能であるプログラムは、プログラムコントロールを保持するコンテナーです。 テナントには、1つ以上のプログラムを含めることができます。  各コントロールは、アクセスレビューをプログラムにリンクして、関連するアクセスレビューを簡単に見つけられるようにします。  

boarded Azure AD アクセスレビューを持つ各テナントには、 `Default program`1 つのプログラムがあります。  グローバル管理者は、コンプライアンスイニシアチブを表すなど、追加のプログラムを作成できます。 


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[プログラムを作成する](../api/program-create.md) |   [アプリケーション](program.md)   |   新しいプログラムを作成します。|
|[プログラムの削除](../api/program-delete.md) |   なし。   |   プログラムを削除します。|
|[プログラムの一覧表示](../api/program-list.md) |  [プログラム](program.md)コレクション|   すべてのプログラムのコレクションを取得します。|
|[プログラムの programcontrols を一覧表示する](../api/program-listcontrols.md) |      [programcontrol](programcontrol.md)コレクション| プログラムのコントロールのコレクションを取得します。|
|[プログラムの更新](../api/program-update.md) |   [アプリケーション](program.md)|  プログラムを更新します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| `id`                        |`String`                              |  プログラムの機能割り当て識別子。                    |
| `displayName`               |`String`                              |  プログラムの名前を指定します。  作成時に必要です。                  |
| `description`               |`String`                              |  プログラムの説明。           |

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
| `controls`                  |[programcontrol](programcontrol.md) | プログラムに関連付けられているコントロール。 |

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.program"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string",
 "description": "string"
}

```

<!--
{
  "type": "#page.annotation",
  "description": "program resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
