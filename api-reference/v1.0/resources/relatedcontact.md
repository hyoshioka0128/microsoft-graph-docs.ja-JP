---
title: その他の連絡先リソースの種類
description: 保護者、支援、医師などの情報を提供する educationUser に関連する連絡先レコード。
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 7e3829de2ffeb073d8360976ce70d13985fcae39
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32579409"
---
# <a name="realtedcontact-resource-type"></a>realtedcontact リソースの種類

保護者、支援、医師などの情報を提供する[educationUser](../resources/educationuser.md)に関連する連絡先レコード。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|String|Azure Active Directory 内の連絡先の id。|
|displayName|String|連絡先の名前。 必須です。|
|emailAddress|String|連絡先のプライマリ電子メールアドレス。|
|mobilePhone|String|連絡先の携帯電話番号。|
|リレーションシップ|`contactRelationship`|ユーザーとの関係。 可能な値`parent`は`relative` `aide` `doctor` `guardian` `other`、、、、、、 `unknownFutureValue`、、です。 `child`|
|accessconsent|Boolean|ユーザーが学生データにアクセスするために同意されているかどうかを示します。|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.relatedContact"
}-->

```json
{
  "id": "String",
  "displayName": "String",
  "emailAddress": "String",
  "mobilePhone": "String",
  "relationship": "contactRelationship",
  "accessConsent": true
}
```

<!-- uuid: 720F9AB6-6E7A-4A66-8B0A-37A556FF99C5
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "relatedContact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
