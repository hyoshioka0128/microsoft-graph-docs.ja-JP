---
title: managedAppStatusRaw リソースの種類
description: 組織アプリの保護と構成についての型指定されていない進捗レポートを表します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 12d451a87012da930bb7330cd8eb63ecaa3fec1f
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34994651"
---
# <a name="managedappstatusraw-resource-type"></a>managedAppStatusRaw リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

組織アプリの保護と構成についての型指定されていない進捗レポートを表します。


[managedAppStatus](../resources/intune-mam-managedappstatus.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[managedAppStatusRaws のリスト](../api/intune-mam-managedappstatusraw-list.md)|[managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) コレクション|[managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[managedAppStatusRaw の取得](../api/intune-mam-managedappstatusraw-get.md)|[managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md)|[managedAppStatusRaw](../resources/intune-mam-managedappstatusraw.md) オブジェクトのプロパティとリレーションシップを読み取ります。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|displayName|String|進捗レポートのフレンドリ名。 [managedAppStatus](../resources/intune-mam-managedappstatus.md) から継承します|
|id|文字列|エンティティのキー。 [managedAppStatus](../resources/intune-mam-managedappstatus.md) から継承します|
|version|String|エンティティのバージョン。 [managedAppStatus](../resources/intune-mam-managedappstatus.md) から継承します|
|content|[Json](../resources/intune-mam-json.md)|進捗レポートの内容。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppStatusRaw"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatusRaw",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```





