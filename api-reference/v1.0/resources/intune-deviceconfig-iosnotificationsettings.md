---
title: iosNotificationSettings リソース タイプ
description: 通知設定を記述するアイテムです。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 3ce016579729353f69f2e7671ff67b5da0004536
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32464590"
---
# <a name="iosnotificationsettings-resource-type"></a>iosNotificationSettings リソース タイプ

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

通知設定を記述するアイテムです。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|bundleID|文字列型 (String)|これらの通知設定を適用するアプリのバンドル ID。|
|appName|String|bundleID に関連するアプリケーション名。|
|publisher|String|bundleID に関連するパブリッシャー。|
|enabled|ブール型 (Boolean)|通知がこのアプリで許可されているかどうかを示します。|
|showInNotificationCenter|Boolean|通知センターに通知を表示できるかどうかを示します。|
|showOnLockScreen|Boolean|ロック画面に通知を表示できるかどうかを示します。|
|alertType|[iosnotificationalerttype](../resources/intune-deviceconfig-iosnotificationalerttype.md)|このアプリの通知用の警告の種類を示します。 可能な値は、`deviceDefault`、`banner`、`modal`、`none` です。|
|badgesEnabled|Boolean|バッジがこのアプリで許可されているかどうかを示します。|
|soundsEnabled|Boolean|サウンドがこのアプリで許可されているかどうかを示します。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNotificationSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNotificationSettings",
  "bundleID": "String",
  "appName": "String",
  "publisher": "String",
  "enabled": true,
  "showInNotificationCenter": true,
  "showOnLockScreen": true,
  "alertType": "String",
  "badgesEnabled": true,
  "soundsEnabled": true
}
```



