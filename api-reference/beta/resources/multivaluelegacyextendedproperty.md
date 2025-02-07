---
title: multiValueLegacyExtendedProperty リソースの種類
description: 値のコレクションが含まれる拡張プロパティ。
localization_priority: Normal
ms.openlocfilehash: 4a30f8cf2a77e43db028c069fc36dc5cd8f360a3
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342185"
---
# <a name="multivaluelegacyextendedproperty-resource-type"></a>multiValueLegacyExtendedProperty リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

値のコレクションが含まれる拡張プロパティ。

オープン拡張機能または拡張プロパティを使用するのに適した状況と、拡張プロパティを指定する方法の詳細については、「[拡張プロパティの概要](../resources/extended-properties-overview.md)」を参照してください。

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Post](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | サポートされているリソースインスタンス: [message](../resources/message.md)、 [mailfolder](../resources/mailfolder.md)、 [event](../resources/event.md)、 [calendar](../resources/calendar.md)、 [contact](../resources/contact.md)、 [contactfolder](../resources/contactfolder.md)、 [outlook の仕事](../resources/outlooktask.md)、または[outlook のタスクフォルダー](../resources/outlooktaskfolder.md)。 グループ[投稿](../resources/post.md) はサポートされていませんので、ご注意ください。 | サポートされているリソースの新しいインスタンスまたは既存のインスタンスに **multiValueLegacyExtendedProperty** を作成します。 |
|[Get](../api/multivaluelegacyextendedproperty-get.md) |サポートされているリソースインスタンス ([message](../resources/message.md)、 [mailfolder](../resources/mailfolder.md)、 [event](../resources/event.md)、 [calendar](../resources/calendar.md)、 [contact](../resources/contact.md)、 [contactfolder](../resources/contactfolder.md)、 [outlook タスク](../resources/outlooktask.md)、 [outlook タスクフォルダー](../resources/outlooktaskfolder.md)、またはグループの[投稿](../resources/post.md)) [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)オブジェクト。 |`$expand` を使用して拡張プロパティでリソース インスタンスを取得します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|string|プロパティ識別子。読み取り専用です。|
|value|string collection|プロパティ値のコレクション。|

## <a name="relationships"></a>リレーションシップ
なし


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty"
}-->

```json
{
  "id": "string (identifier)",
  "value": ["string"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "multiValueLegacyExtendedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
