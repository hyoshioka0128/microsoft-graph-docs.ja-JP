---
title: managedAppOperation リソースの種類
description: アプリ登録に対して適用される操作を表します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 045ce9f78f8a2de5e14bbe974cea2d6cc1aa7c6a
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34994784"
---
# <a name="managedappoperation-resource-type"></a>managedAppOperation リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

アプリ登録に対して適用される操作を表します。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List managedAppOperations](../api/intune-mam-managedappoperation-list.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md) コレクション|[managedAppOperation](../resources/intune-mam-managedappoperation.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get managedAppOperation](../api/intune-mam-managedappoperation-get.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create managedAppOperation](../api/intune-mam-managedappoperation-create.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|新しい [managedAppOperation](../resources/intune-mam-managedappoperation.md) オブジェクトを作成します。|
|[Delete managedAppOperation](../api/intune-mam-managedappoperation-delete.md)|なし|[managedAppOperation](../resources/intune-mam-managedappoperation.md) を削除します。|
|[Update managedAppOperation](../api/intune-mam-managedappoperation-update.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|displayName|String|操作名。|
|lastModifiedDateTime|DateTimeOffset|アプリ操作が変更された最終時刻。|
|state|String|操作の現在の状態。|
|id|文字列|エンティティのキー。|
|version|文字列型 (String)|エンティティのバージョン。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppOperation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "state": "String",
  "id": "String (identifier)",
  "version": "String"
}
```





