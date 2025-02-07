---
title: oAuth2PermissionGrant リソースの種類
description: ユーザーまたは管理者の同意プロセスの一部としてアプリケーション (サービスプリンシパルによって表される) に付与された OAuth 2.0 スコープ (デリゲートされたアクセス許可) を表します。
localization_priority: Normal
ms.openlocfilehash: f23d2e7a8b57b324a92a1268ab4cc0393d8906f0
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342066"
---
# <a name="oauth2permissiongrant-resource-type"></a>oAuth2PermissionGrant リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

ユーザーまたは管理者の同意プロセスの一部としてアプリケーション (サービスプリンシパルによって表される) に付与された OAuth 2.0 スコープ (デリゲートされたアクセス許可) を表します。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.oAuth2PermissionGrant"
}-->

```json
{
  "clientId": "string",
  "consentType": "string",
  "expiryTime": "String (timestamp)",
  "id": "string (identifier)",
  "principalId": "string",
  "resourceId": "string",
  "scope": "string",
  "startTime": "String (timestamp)"
}

```
## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|clientId|String| リソースにアクセスするときにユーザーを偽装する同意を付与するサービスプリンシパルの id (resourceId プロパティで表されます)。 |
|consentType|String| 同意が管理者によって (組織の代わりに) 提供されたか、個人によって提供されたかを示します。 使用可能な値は*allprincipals*または*Principal*です。 |
|expiryTime|DateTimeOffset| 現時点では、有効期限の値は無視されます。 |
|id|文字列型 (String)| 一意の識別子。 読み取り専用です。|
|principalId|String| consettings type が*allprincipals*の場合、この値は null になり、組織内のすべてのユーザーに同意が適用されます。 conな種類が*Principal*の場合、このプロパティは同意を付与されたユーザーの id を指定し、そのユーザーに対してのみ適用されます。 |
|resourceId|String| アクセスが許可されているリソースサービスプリンシパルの id を指定します。 |
|scope|文字列| OAuth 2.0 アクセストークンでリソースアプリケーションが想定する[スコープ](/graph/permissions-reference)要求の値を指定します。 たとえば、「ユーザー」と表示*します。* |
|startTime|DateTimeOffset| 現時点では、開始時刻の値は無視されます。 |

## <a name="relationships"></a>リレーションシップ
なし


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[oAuth2PermissionGrant を取得する](../api/oauth2permissiongrant-get.md) | [oAuth2PermissionGrant](oauth2permissiongrant.md) |oAuth2PermissionGrant オブジェクトのプロパティとリレーションシップを読み取ります。|
|[リスト oAuth2PermissionGrants](../api/oauth2permissiongrant-list.md) | [oAuth2PermissionGrant](oauth2permissiongrant.md) コレクション | oauth2PermissionGrant オブジェクトのリストを取得します。 |
|[oAuth2PermissionGrant の更新](../api/oauth2permissiongrant-update.md) | [oAuth2PermissionGrant](oauth2permissiongrant.md) |oAuth2PermissionGrant オブジェクトを更新します。 |
|[oAuth2PermissionGrant の削除](../api/oauth2permissiongrant-delete.md) | なし |oAuth2PermissionGrant オブジェクトを削除します。 |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "oAuth2PermissionGrant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
