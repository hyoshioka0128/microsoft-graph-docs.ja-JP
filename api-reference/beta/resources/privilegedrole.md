---
title: privilegedRole リソースの種類
description: Azure AD 管理者の役割 (**全体管理者、課金管理者、サービス管理者、ユーザー管理者、パスワード管理者**など) を表します。
localization_priority: Normal
ms.openlocfilehash: 9b5454745257bea071f967b654d3b6174c3c3289
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33344292"
---
# <a name="privilegedrole-resource-type"></a>privilegedRole リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Azure AD 管理者の役割 (**全体管理者、課金管理者、サービス管理者、ユーザー管理者、パスワード管理者**など) を表します。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[privilegedRole オブジェクトを一覧表示する](../api/privilegedrole-list.md) | [privilegedRole](privilegedrole.md)コレクション|privilegedRole のコレクションを取得します。|
|[privilegedRole を取得する](../api/privilegedrole-get.md) | [privilegedRole](privilegedrole.md) |privilegedRole オブジェクトのプロパティとリレーションシップを読み取ります。|
|[割り当てを一覧表示する](../api/privilegedrole-list-assignments.md) |[privilegedRoleAssignment](privilegedroleassignment.md)コレクション| このロールの割り当てオブジェクトのコレクションを取得します。|
|[selfactivate](../api/privilegedrole-selfactivate.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|割り当てられた役割をアクティブ化します。|
|[selfdeactivate](../api/privilegedrole-selfdeactivate.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|割り当てられた役割を非アクティブ化します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|string|管理者の役割の一意識別子。 これは GUID 文字列であり、指定された役割に対して Azure AD からのロールテンプレート id と同じ値を持ちます。 読み取り専用。|
|name|string|役割名。|

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|assignments|[privilegedRoleAssignment](privilegedroleassignment.md)コレクション| この役割の割り当て。 読み取り専用です。 Null 許容型。|
|settings|[privilegedRoleSettings](privilegedrolesettings.md)| この役割の設定。 読み取り専用です。 Null 許容型。|
|summary|[privilegedRoleSummary](privilegedrolesummary.md)| このロールの概要情報。 読み取り専用です。 Null 許容型。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",
  "@odata.type": "microsoft.graph.privilegedRole"
}-->

```json
{
  "id": "string (identifier)",
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "privilegedRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
