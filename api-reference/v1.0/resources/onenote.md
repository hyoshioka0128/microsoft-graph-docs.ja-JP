---
title: OneNote リソースの種類
description: OneNote リソースのエントリ ポイントです。
author: jewan-microsoft
localization_priority: Priority
ms.prod: onenote
ms.openlocfilehash: 8240336bfcb9e45e33172c2c1551b71a65c315e0
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32462803"
---
# <a name="onenote-resource-type"></a>OneNote リソースの種類

OneNote リソースのエントリ ポイントです。

Microsoft Graph API を介しての OneNote サービスに対する呼び出しすべては、次のサービス ルート URL を使用します。

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

Office 365 またはコンシューマー OneDrive のユーザー ノートブック、Office 365 のグループ ノートブック、または SharePoint サイトでホストされているチームのノートブックを場所として指定できます。 

**ユーザー ノートブック** コンシューマー OneDrive または OneDrive for Business の個人用ノートブックにアクセスするには、次の URL のいずれかを使用します。

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

**グループ ノートブック** グループによって所有されているノートブックにアクセスするには、次のサービス ルート URL を使用します。

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
**SharePoint サイト ノートブック** SharePoint チーム サイトによって所有されているノートブックにアクセスするには、次のサービス ルート URL を使用します。

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
## <a name="authorization"></a>承認

OneNote API で動作するために必要なアクセス許可については、「[メモのアクセス許可](/graph/permissions-reference#notes-permissions)」を参照してください。


## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|notebooks|[Notebook](notebook.md) collection|ユーザーまたはグループが所有している OneNote ノートブックのコレクションです。 読み取り専用。 Null 許容型。|
|operations|[OnenoteOperation](onenoteoperation.md) コレクション |OneNote の操作の状態です。 操作のコレクションを取得することはサポートされていませんが、応答で `Operation-Location` ヘッダーが返される場合には長時間実行処理の状態を取得できます。 読み取り専用。 Null 許容型。|
|ページ|[OnenotePage](page.md)コレクション|ユーザーまたはグループが所有しているすべての OneNote ノートブックのページです。  読み取り専用。 Null 許容型。|
|リソース|[OnenoteResource](resource.md) コレクション |OneNote ページの画像リソースおよび他のファイル リソースです。 リソース コレクションを取得することはサポートされていませんが、[特定のリソースのバイナリ コンテンツを取得](resource.md)できます。 読み取り専用。 Null 許容型。|
|sectionGroups|[SectionGroup](sectiongroup.md) collection|ユーザーまたはグループが所有しているすべての OneNote ノートブックのセクション グループです。  読み取り専用。 Null 許容型。|
|セクション|[OnenoteSection](section.md) コレクション|ユーザーまたはグループが所有しているすべての OneNote ノートブック内のセクションです。  読み取り専用。 Null 許容型。|

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Create notebook](../api/onenote-post-notebooks.md) |[Notebook](notebook.md)| ノートブックのコレクションに投稿してノートブックを作成します。|
|[List notebooks](../api/onenote-list-notebooks.md) |[Notebook](notebook.md) collection| ノートブックのコレクションを取得します。|
|[Create page](../api/onenote-post-pages.md) |[Page](page.md)| ページのコレクションに投稿してページを作成します。|
|[List pages](../api/onenote-list-pages.md) |[Page](page.md) collection| ページのコレクションを取得します。|
|[List section groups](../api/onenote-list-sectiongroups.md) |[SectionGroup](sectiongroup.md) collection| セクション グループのコレクションを取得します。|
|[List sections](../api/onenote-list-sections.md) |[OnenoteSection](section.md) コレクション| セクションのコレクションを取得します。|


## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.onenote"
}-->
``` json
{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenote resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
