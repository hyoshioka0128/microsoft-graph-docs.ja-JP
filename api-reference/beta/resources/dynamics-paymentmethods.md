---
title: paymentMethods リソースの種類
description: Dynamics 365 Business Central の支払い方法オブジェクト。
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
localization_priority: Normal
ms.prod: dynamics-365-business-central
ms.openlocfilehash: 1e4cd044d4b552a9239b742efb302633524ce22b
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32507246"
---
# <a name="paymentmethods-resource-type"></a>paymentMethods リソースの種類
は、PayPal、クレジットカード、銀行口座など、Dynamics 365 Business Central の支払方法を表します。

## <a name="methods"></a>メソッド

| メソッド                                                          | 戻り値の型  |説明             |
|:----------------------------------------------------------------|:-------------|:-----------------------|
|[paymentMethods を取得する](../api/dynamics-paymentmethods-get.md)      |paymentMethods|支払い方法オブジェクトを取得します。   |
|[Post paymentMethods](../api/dynamics-create-paymentmethods.md)  |paymentMethods|支払い方法オブジェクトを作成します。|
|[Patch paymentMethods](../api/dynamics-paymentmethods-update.md) |paymentMethods|支払い方法オブジェクトを更新します。|
|[paymentMethods の削除](../api/dynamics-paymentmethods-delete.md)|なし          |支払い方法オブジェクトを削除します。|

## <a name="properties"></a>プロパティ
| プロパティ           | 型   |説明                                                  |
|:-------------------|:-------|:------------------------------------------------------------|
|id                  |GUID    |paymentMethods の一意の ID。 編集できません。           |
|code                |string  |支払い方法のコードを指定します。                           |
|displayName         |string  |支払い方法の表示名を指定します。                   |
|lastModifiedDateTime|datetime|支払い方法が最後に変更された datetime。 読み取り専用。|  


## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記

paymentMethods の JSON 表記を次に示します。


```json
{
  "id": "GUID",
  "code": "string",
  "displayName": "string",
  "lastModifiedDateTime": "datetime"
}

```
