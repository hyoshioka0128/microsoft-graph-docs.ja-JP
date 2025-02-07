---
title: エンドポイントリソースの種類
description: 'エンドポイントは、エンティティに関連付けられているリソースの url を表します。  たとえば、新しい office 365 グループを作成すると、その他のリソースも office 365 グループの一部として作成されます。 これには、会話のグループメールボックスや、ドキュメントやファイルのグループ OneDrive フォルダーなどが含まれます。 これらの Office 365 グループリソースの詳細については、「グループリソースの種類の*エンドポイント*ナビゲーションを使用して、関連付けられたリソース url」を参照してください。 これにより、アプリケーションはこれらのリソースを理解し、リソース URL エクスペリエンスを独自のエクスペリエンスに埋め込むこともできます。 '
localization_priority: Normal
ms.openlocfilehash: 474da77d10d9b433dd6d4914f9b75812e040a9e4
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33340211"
---
# <a name="endpoint-resource-type"></a>エンドポイントリソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

エンドポイントは、エンティティに関連付けられているリソースの url を表します。  たとえば、新しい office 365 グループを作成すると、その他のリソースも office 365 グループの一部として作成されます。 これには、会話のグループメールボックスや、ドキュメントやファイルのグループ OneDrive フォルダーなどが含まれます。 これらの Office 365 グループリソースの詳細については、「グループリソースの種類の*エンドポイント*ナビゲーションを使用して、関連付けられたリソース url」を参照してください。 これにより、アプリケーションはこれらのリソースを理解し、リソース URL エクスペリエンスを独自のエクスペリエンスに埋め込むこともできます。 

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[エンドポイントを一覧表示する](../api/group-list-endpoints.md) |[Endpoint](endpoint.md) collection| endpoint オブジェクトのコレクションを取得します。 |
|[エンドポイントを取得する](../api/endpoint-get.md) | [エンドポイント](endpoint.md) |endpoint オブジェクトのプロパティと関係を読み取ります。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| capability     | String  | このリソースに関連付けられている機能について説明します。 (例: メッセージ、会話など) null 許容ではありません。 読み取り専用です。 |
| id             | String  | エンドポイントの一意の識別子。要点. null 許容型ではありません。 読み取り専用です。|
| providerId     | String  | 発行元のサービスのアプリケーション id。 null 許容型ではありません。 読み取り専用です。|
| プロバイダー   | String  | 発行元のサービスの名前。 読み取り専用です。|
| providerresourceid|String| Office 365 グループの場合は、リソースの既知の名前 (たとえば、FeedURL など) に設定されます。 null 許容型ではありません。 読み取り専用です。|
| uri            | String  | 発行されたリソースの URL。 null 許容型ではありません。 読み取り専用です。|

## <a name="relationships"></a>リレーションシップ

なし。


## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.endpoint"
}-->

```json
{
  "capability": "String",
  "id": "String (identifier)",
  "providerId": "String",
  "providerName": "String",
  "providerResourceId": "String",
  "uri": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Endpoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
