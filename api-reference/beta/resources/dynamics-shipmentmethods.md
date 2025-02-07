---
title: shipmentMethods リソースの種類
description: Dynamics 365 Business Central の出荷方法。
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
localization_priority: Normal
ms.prod: dynamics-365-business-central
ms.openlocfilehash: 2f7ef9611fc85c13ac24c79b292e06a6bdc5d587
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32543036"
---
# <a name="shipmentmethods-resource-type"></a>shipmentMethods リソースの種類
UPS、Fedex、DHL など、Dynamics 365 Business Central の出荷方法を表します。

## <a name="methods"></a>メソッド

| メソッド       | 戻り値の型  |説明|
|:---------------|:--------|:----------|
|[shipmentMethods を取得する](../api/dynamics-shipmentmethods-get.md)|shipmentMethods|送付方法を取得します。|
|[Post shipmentMethods](../api/dynamics-create-shipmentmethods.md)|shipmentMethods|送付方法を作成します。|
|[Patch shipmentMethods](../api/dynamics-shipmentmethods-update.md)|shipmentMethods|送付方法を更新します。|
|[shipmentMethods の削除](../api/dynamics-shipmentmethods-delete.md)|なし|送付方法を削除します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|GUID|shipmentMethod の一意の ID。 編集できません。|
|code|string|送付方法のコードを指定します。|
|displayName|string|送付方法の表示名を指定します。|
|lastModifiedDateTime|datetime|出荷方法が最後に変更された日付です。 読み取り専用。|  


## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記

shipmentMethod の JSON 表記を次に示します。

```json
{
  "id": "GUID",
  "code": "string",
  "displayName": "string",
  "lastModifiedDateTime": "datetime"
}

```


