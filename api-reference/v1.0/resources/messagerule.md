---
title: messageRule リソースの種類
description: ユーザーの受信トレイ内のメッセージに適用されるルールです。
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: a1a1ed26b7f0e659af0b7aeebae7f6da456afddf
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32580290"
---
# <a name="messagerule-resource-type"></a>messageRule リソースの種類


ユーザーの受信トレイ内のメッセージに適用されるルールです。

Outlook では、受信トレイ内の受信メッセージに対し、一定の条件に基づいて特定の操作を実行するルールを設定できます。 

プログラムでこれらのルールにアクセスするには、受信トレイの [フォルダー](mailfolder.md)の **messageRules** ナビゲーション プロパティを使用します。 各ルールは **messageRule** リソース、利用可能なルールの処理は [messageRuleActions](messageruleactions.md) 複合型、利用可能なルール条件および例外は [messageRulePredicates](messagerulepredicates.md) 複合型で表されます。


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| actions | [messageRuleActions](messageruleactions.md) | 該当する条件が満たされた場合にメッセージに対して実行されるアクション。 |
| conditions | [messageRulePredicates](messagerulepredicates.md) | 該当するルール アクションをトリガーするために満たす必要のある条件。 |
| displayName | String | ルールの表示名。 |
| exceptions | [messageRulePredicates](messagerulepredicates.md) | ルールの例外条件。 |
| hasError | Boolean | ルールがエラー状態かどうかを示します。 読み取り専用です。 |
| id |String|ルールの一意識別子。 読み取り専用。|
| isEnabled | Boolean | メッセージに対するルールの適用が有効になっているかどうかを示します。 |
| isReadOnly | Boolean | ルールが読み取り専用のため、ルールの REST API による変更や削除ができないことを示します。 |
| sequence | Int32 | 他のルールもある中で、そのルールが実行される順序を示します。 |


## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
   "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.messageRule"
}-->

```json
{
  "actions": {"@odata.type": "microsoft.graph.messageRuleActions"},
  "conditions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "displayName": "String",
  "exceptions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "hasError": "Boolean",
  "id": "String",
  "isEnabled": "Boolean",
  "isReadOnly": "Boolean",
  "sequence": "Int32"
}

```

## <a name="methods"></a>メソッド
| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[ルールの一覧表示](../api/mailfolder-list-messagerules.md) | [messageRule](messagerule.md) コレクション |ユーザーの受信トレイに定義されているすべての **messageRule** オブジェクトを取得します。|
|[ルールの取得](../api/messagerule-get.md) | [messageRule](messagerule.md) |**messageRule** オブジェクトのプロパティとリレーションシップを読み取ります。|
|[作成](../api/mailfolder-post-messagerules.md) | [messageRule](messagerule.md) |条件とアクションのセットを指定して **messageRule** オブジェクトを作成します。|
|[更新](../api/messagerule-update.md) | [messageRule](messagerule.md) |**messageRule** オブジェクトの書き込み可能なプロパティを変更し、変更を保存します。 |
|[削除](../api/messagerule-delete.md) | なし |指定した **messageRule** オブジェクトを削除します。 |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
