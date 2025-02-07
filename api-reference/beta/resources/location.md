---
title: Location リソースの種類
description: イベントの場所の情報を表します。
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: ba7be26bc1a96d684ae5c2c5b21921def3273d70
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345376"
---
# <a name="location-resource-type"></a>Location リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[イベント](event.md)の場所の情報を表します。

カレンダー内にイベントを作成するには、複数の方法があります。たとえば、アプリで[イベント作成](../api/user-post-events.md) REST API を使用するという方法、Outlook ユーザー インターフェイスを手動で使用するという方法などです。 ユーザー インターフェイスを使用してイベントを作成する場合は、場所をプレーン テキストとして指定することも、Outlook、[Bing Autosuggest](https://blogs.bing.com/search/2013/02/20/a-look-at-autosuggest/)、または [Bing ローカル検索](https://blogs.bing.com/search/2010/08/17/local-search-on-m-bing-com/)で提供される会議室リストから選択して指定することもできます。 

イベントの作成方法によって、Outlook は読み取り専用の **locationType** プロパティを異なる方法で設定します。 

| イベントの作成方法  | プロパティ   | 予期される値 |
|:----------|:-------|:--------------------------------|
| [イベント作成](../api/user-post-events.md) REST API | **locationType** | `default` |
| Outlook のユーザー インターフェイス | **locationType** | 以下のいずれか: <ul><li>プレーン テキストとして入力された場所の場合は `default`。</li><li>Outlook の会議室リストで提供された会議室の場合は `conferenceRoom`。</li><li>Bing Autosuggest または Bing ローカル検索による場所の場合は、`homeAddress`、`businessAddress`、`geoCoordinates`、`streetAddress`、`hotel`、`restaurant`、`localBusiness`、`postalAddress` のいずれか。</li></ul> |




## <a name="properties"></a>プロパティ
| プロパティ  | 型   | 説明                                                     |
|:----------|:-------|:----------------------------------------------------------------|
| address | [physicalAddress](physicaladdress.md) |場所の番地。 |
| coordinates | [outlookGeoCoordinates](outlookgeocoordinates.md) | 場所の地理的座標と標高。 |
| displayName  | String | 場所に関連付けられた名前。                       |
| locationEmailAddress | String | 場所のメール アドレス (省略可能)。 |
| locationUri | String | 場所を表す URI (省略可能)。 |
| locationType | locationType | 場所の種類。 可能な値は、`default`、`conferenceRoom`、`homeAddress`、`businessAddress`、`geoCoordinates`、`streetAddress`、`hotel`、`restaurant`、`localBusiness`、`postalAddress` です。 読み取り専用。|
| uniqueId | String | 内部使用のために用意されています。|
| uniqueIdType | String | 内部使用のみ。 |


## <a name="json-representation"></a>JSON 表記

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.location"
}-->
```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "coordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "displayName": "string",
  "locationEmailAddress": "string",
  "locationType": "string",
  "locationUri": "string",
  "uniqueId": "string",
  "uniqueIdType": "string"
}

```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "location resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
