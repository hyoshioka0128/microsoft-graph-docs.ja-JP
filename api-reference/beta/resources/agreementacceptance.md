---
title: agreementAcceptance リソースの種類
description: azure Active Directory (azure AD) によって提供される会社のカスタマイズ可能な使用条件の範囲内でのユーザーの現在の状態を表します。
localization_priority: Normal
ms.openlocfilehash: 84b54998e8afaad501d2cf46d564400aa2307507
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33339148"
---
# <a name="agreementacceptance-resource-type"></a>agreementAcceptance リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

azure Active Directory (azure AD) によって提供される会社のカスタマイズ可能な使用条件の範囲内でのユーザーの現在の状態を表します。

<!--
## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get agreementAcceptance](../api/agreementacceptance-get.md) | [agreementAcceptance](agreementacceptance.md) | Read properties and relationships of agreementAcceptance object. |
| [Update](../api/agreementacceptance-update.md) | [agreementAcceptance](agreementacceptance.md) | Update an **agreementAcceptance** object. |
| [Delete](../api/agreementacceptance-delete.md) | None | Delete an **agreementAcceptance** object. |
-->

## <a name="properties"></a>プロパティ
| プロパティ     | 型        | 説明 |
|:-------------|:------------|:------------|
|agreementFileId|String|ユーザーによって承認されたアグリーメントファイルの ID。|
|agreementId|String|契約の ID。|
|id|String| 読み取り専用です。|
|recordedDateTime|DateTimeOffset|Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|
|state|string| 可能な値は、`accepted`、`declined` です。|
|userDisplayName|String|承諾が記録されたときのユーザーの表示名。|
|userEmail|String|承諾が記録されたユーザーの電子メール。|
|userId|String|契約書を受諾したユーザーの ID。|
|userPrincipalName|String|承諾が記録されたユーザーの UPN。|

## <a name="relationships"></a>リレーションシップ
なし


## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementAcceptance"
}-->

```json
{
  "agreementFileId": "String",
  "agreementId": "String",
  "id": "String (identifier)",
  "recordedDateTime": "String (timestamp)",
  "state": "string",
  "userDisplayName": "String",
  "userEmail": "String",
  "userId": "String",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "agreementAcceptance resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
