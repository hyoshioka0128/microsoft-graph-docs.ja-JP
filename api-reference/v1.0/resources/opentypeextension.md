---
title: openTypeExtension リソース タイプ (オープン拡張機能)
description: オープン拡張 (旧称は Office 365 のデータ拡張機能) を使用すると、型指定されていないプロパティを Microsoft Graph のリソースに簡単に直接追加できます。
localization_priority: Priority
author: dkershaw10
ms.openlocfilehash: 854897e1cc4d887fc0f4d2f184a4e745e5cdc468
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32462635"
---
# <a name="opentypeextension-resource-type-open-extensions"></a>openTypeExtension リソース タイプ (オープン拡張)

オープン拡張 (旧称は Office 365 のデータ拡張機能) を使用すると、型指定されていないプロパティを Microsoft Graph のリソースに簡単に直接追加できます。

オープン拡張機能は、**openTypeExtension** リソースで表されます。 リソースに追加されるオープン拡張機能は **extensions** ナビゲーション プロパティに表示されます。このプロパティは、[extension](extension.md) 抽象型から派生します。 各拡張機能には **extensionName** プロパティがあります。このプロパティは、すべての拡張機能とカスタム データで唯一定義済みの書き込み可能なプロパティです。

拡張機能名が必ず一意であるようにする方法の 1 つは、_独自のドメイン_に依存する逆引きドメイン ネーム システム (DNS) 形式 (例: `Com.Contoso.ContactInfo`) を使用することです。 拡張機能名に Microsoft ドメイン (`Com.Microsoft` または `Com.OnMicrosoft`) を使用しないでください。

オープン拡張機能の例:[オープン拡張機能を使用したユーザーへのカスタム データの追加](/graph/extensibility-open-users)

オープン拡張機能は、次のリソースの対応するバージョンの一般提供 (GA: /v1.0 および /ベータ) またはプレビュー (/ベータ) でサポートされています。

|リソース |バージョン |
|:---------------|:-------|
| [管理単位](/graph/api/resources/administrativeunit?view=graph-rest-beta)  | プレビューのみ |
| [予定表イベント](event.md) | GA |
| グループ[予定表イベント](event.md) | GA |
| グループ会話スレッド[投稿](post.md) | GA |
| [device](device.md) | GA |
| [グループ](group.md) | GA |
| [メッセージ](message.md) | GA |
| [組織](organization.md) | GA |
| [個人用連絡先](contact.md) | GA |
| [ユーザー](user.md) | GA |

## <a name="outlook-specific-considerations"></a>Outlook 固有の考慮事項

Outlook リソース (イベント、メッセージ、個人用連絡先) に存在する各オープン拡張は、[MAPI 名前付きプロパティ](https://msdn.microsoft.com/library/cc765864(v=office.15).aspx)に保存されます。 Outlook のオープン拡張を作成する場合は、MAPI 名前付きプロパティがユーザーのメールボックスで有限のリソースであることを考慮してください。 ユーザーの名前付きプロパティのクォータがすべて使用されると、それ以上、そのユーザーに対して名前付きのプロパティを作成することはできません。 これにより、機能する名前付きプロパティに依存しているクライアントから、予期しない動作が発生する可能性があります。

Outlook リソースのオープン拡張を作成する場合は、次のガイドラインを適用します。

- 必要な拡張機能の最小数を作成します。 ほとんどのアプリケーションで必要な拡張機能は、1 つのみです。 拡張機能には、定義済みのプロパティや構造体が設定されていないため、1 つの拡張機能に複数の値を保存できます。
- 拡張機能には変更可能な方法 (ユーザー入力に基づくなど) で名前を付けないでください。 ユーザーのメールボックスで以前に使用されていない新しい名前でオープン拡張が作成されるたびに、新しい MAPI 名前付きプロパティが作成されます。 拡張機能を削除しても、名前付きプロパティは削除されません。

### <a name="use-open-extensions-for-outlook-resources-or-extended-properties"></a>オープン拡張 (Outlook リソース用) または拡張プロパティを使用する

オープン拡張は、カスタム データの保存およびカスタム データへのアクセスを必要とするほとんどのシナリオに対して推奨されるソリューションです。 ただし、[拡張プロパティとこの REST API](extended-properties-overview.md) は、[Microsoft Graph API のメタデータ](https://developer.microsoft.com/graph/docs/overview/call_api)を通じてまだ公開されていない Outlook MAPI プロパティのカスタム データにアクセスする必要がある場合に使用できます。 メタデータが公開するプロパティは、[https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata) で確認できます。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "baseType": "microsoft.graph.extension",
  "@odata.type": "microsoft.graph.openTypeExtension"
}-->

```json
{
  "extensionName": "string",
  "id": "string (identifier)"
}

```

## <a name="properties"></a>プロパティ

|プロパティ | 型 | 説明 |
|:---------------|:--------|:----------|
|extensionName|String|オープン型のオープン拡張機能の一意のテキスト識別子。必須。|
|id|String| **extensionName** と拡張子タイプを連結する完全修飾識別子。読み取り専用。|

## <a name="relationships"></a>リレーションシップ

なし

## <a name="methods"></a>メソッド

|メソッド | 戻り値の型 | 説明 |
|:---------------|:--------|:----------|
|[Post](../api/opentypeextension-post-opentypeextension.md) | (既存リソースのインスタンス内の) [openTypeExtension](opentypeextension.md)、または、openTypeExtension オブジェクトを含む新しい[contact](../resources/contact.md)、[event](../resources/event.md)、[message](../resources/message.md)。 | 既存または新規のリソース インスタンス内に openTypeExtension オブジェクトを作成します。|
|[Get](../api/opentypeextension-get.md) | [openTypeExtension](opentypeextension.md) |openTypeExtension オブジェクトのプロパティと関係を読み取ります。|
|[Update](../api/opentypeextension-update.md) | [openTypeExtension](opentypeextension.md) |openTypeExtension オブジェクトを更新します。 |
|[Delete](../api/opentypeextension-delete.md) | なし |openTypeExtension オブジェクトを削除します。 |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
