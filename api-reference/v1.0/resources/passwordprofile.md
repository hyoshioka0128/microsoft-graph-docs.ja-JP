---
title: passwordProfile リソースの種類
description: ユーザーに関連付けられているパスワードのプロファイルが含まれています。ユーザー エンティティの **PasswordProfile** プロパティは、**passwordProfile** オブジェクトです。
localization_priority: Priority
ms.openlocfilehash: cea8dcc114cb599a2d857ced67ac25c9eb275497
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32462502"
---
# <a name="passwordprofile-resource-type"></a>passwordProfile リソースの種類

ユーザーに関連付けられているパスワードのプロファイルが含まれています。[ユーザー](user.md) エンティティの **PasswordProfile** プロパティは、**passwordProfile** オブジェクトです。


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|forceChangePasswordNextSignIn|Boolean| ユーザーが次回のログインでパスワードを変更する必要がある場合は **true**、それ以外の場合は **false**。 |
|forceChangePasswordNextSignInWithMfa|Boolean| **true** の場合、次回のサインイン時にユーザーは、パスワードの変更を強制される前に多要素認証 (MFA) を実行する必要があります。 この動作は **forceChangePasswordNextSignIn** と同じですが、パスワードを変更する前にユーザーが多要素認証を実行する必要がある点が異なります。 パスワードを変更すると、このプロパティは自動的に **false** にリセットされます。 設定しない場合、既定値は **false** です。 |
|パスワード|String|ユーザーのパスワード。このプロパティは、ユーザーの作成時に必要です。このプロパティは更新できますが、ユーザーは次回のログインでパスワードを変更する必要があります。パスワードは、ユーザーの **passwordPolicies** プロパティによって指定されているとおりの最小要件を満たす必要があります。既定では、強力なパスワードが必要です。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordProfile"
}-->

```json
{
  "forceChangePasswordNextSignIn": true,
  "forceChangePasswordNextSignInWithMfa": false,
  "password": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordProfile resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
