---
title: keycredential リソースの種類
description: アプリケーションまたはサービスプリンシパルに関連付けられているキーの資格情報を含みます。 application エンティティおよび serviceprincipal エンティティの**keycredentials**プロパティは**keycredentials**のコレクションです。
localization_priority: Normal
ms.openlocfilehash: 312821a91bdbb1ad15e136d2b7fc8f9184df4eac
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345387"
---
# <a name="keycredential-resource-type"></a>keycredential リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

アプリケーションまたはサービスプリンシパルに関連付けられているキーの資格情報を含みます。 [application](application.md)エンティティおよび[serviceprincipal](serviceprincipal.md)エンティティの**keycredentials**プロパティは**keycredentials**のコレクションです。


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.keyCredential"
}-->

```json
{
  "customKeyIdentifier": "binary",
  "endDateTime": "String (timestamp)",
  "keyId": "guid",
  "startDateTime": "String (timestamp)",
  "type": "string",
  "usage": "string",
  "key": "binary"
}

```
## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|customkeyidentifier|Binary| カスタムキー識別子 |
|endDateTime|DateTimeOffset|資格情報の有効期限が切れる日付と時刻。Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、常に UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|
|id|Guid|キーの一意識別子 (GUID)。|
|startDateTime|DateTimeOffset|資格情報が有効になる日時。Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、常に UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|
|type|String|キーの資格情報の種類。たとえば、"Symmetric" となります。|
|上|String|キーを使用できる目的を記述する文字列。たとえば、"Verify" とします。|
|key|Binary|            |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "keyCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
