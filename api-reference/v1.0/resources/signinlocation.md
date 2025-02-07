---
title: signInLocation リソースの種類
description: サインインが行われた場所から、市区町村、都道府県、および国/地域を提供します。
localization_priority: Normal
author: dhanyahk
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6f81556526c9de1177248b7015bb276e47cb73d9
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2019
ms.locfileid: "33629237"
---
# <a name="signinlocation-resource-type"></a>signInLocation リソースの種類

サインインが行われた場所から、市区町村、都道府県、および国/地域を提供します。

## <a name="properties"></a>プロパティ

| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|city|String|サインインが発生した都市を提供します。 これは、サインインアクティビティの緯度/経度情報を使用して計算されます。|
|countryOrRegion|String|サインインが発生した国コード情報 (2 文字コード) を提供します。  これは、サインインアクティビティの緯度/経度情報を使用して計算されます。|
|geoCoordinates|[geoCoordinates](geocoordinates.md)|サインインしたときの緯度、経度、高度を提供します。|
|state|String|サインインが開始された状態を提供します。 これは、サインインアクティビティの緯度/経度情報を使用して計算されます。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInLocation"
}-->

```json
{
  "city": "String",
  "countryOrRegion": "String",
  "geoCoordinates": {"@odata.type": "microsoft.graph.geoCoordinates"},
  "state": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInLocation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
