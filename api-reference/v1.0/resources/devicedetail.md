---
title: deviceDetail リソースの種類
description: サインインに使用するデバイスに関連付けられているデバイスの詳細を示します。 これには、デバイスブラウザーとオペレーティングシステム、デバイスが Azure AD で管理されているかどうかなどの情報が含まれます。
localization_priority: Normal
author: dhanyahk
ms.prod: microsoft-identity-platform
ms.openlocfilehash: a6ea50eeea3a906346b69466d2686a2de101792a
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2019
ms.locfileid: "33629300"
---
# <a name="devicedetail-resource-type"></a>deviceDetail リソースの種類

サインインに使用するデバイスに関連付けられているデバイスの詳細を示します。 これには、デバイスブラウザーとオペレーティングシステム、デバイスが Azure AD で管理されているかどうかなどの情報が含まれます。

## <a name="properties"></a>プロパティ

| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|ブラウザー|String|サインインに使用するのブラウザー情報を示します。|
|deviceId|String|サインインに使用されているデバイスの UniqueID を参照します。|
|displayName|String|サインインに使用されているデバイスの名前を参照します。|
|isCompliant|Boolean|デバイスが準拠しているかどうかを示します。|
|isManaged|ブール値|デバイスが管理されているかどうかを示します。|
|operatingSystem|String|サインインに使用するオペレーティングシステムの名前とバージョンを示します。|
|trustType|文字列|サインインしているデバイスが、Workplace Join、AzureAD Join、ドメインに参加しているかどうかに関する情報を提供します。 |

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.deviceDetail"
}-->

```json
{
  "browser": "String",
  "deviceId": "String",
  "displayName": "String",
  "isCompliant": true,
  "isManaged": true,
  "operatingSystem": "String",
  "trustType": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "deviceDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
