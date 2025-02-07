---
title: deviceManagementSettings リソースの種類
description: まだ文書化されていません
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: a087192b9ff46b79f5f585cc9515b9c78d806e99
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34990009"
---
# <a name="devicemanagementsettings-resource-type"></a>deviceManagementSettings リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

まだ文書化されていません

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|deviceComplianceCheckinThresholdDays|Int32|デバイスがチェックインせずに移動し、準拠性を維持できる日数です。 有効な値は 0 から 120 までです|
|isScheduledActionEnabled|Boolean|ルールのスケジュール済みアクションの機能が有効かどうか。|
|secureByDefault|Boolean|これが true の場合に、対象となるコンプライアンス ポリシーがないと、デバイスは非準拠となります|
|enhancedJailBreak|Boolean|拡張 jailbreak 検出では、機能が有効または無効になっています。|
|deviceInactivityBeforeRetirementInDay|Int32|指定した日数が経過してもデバイスがチェックインされない場合は、会社のデータが削除されている可能性があり、デバイスは管理下にありません。 有効な値は 30 ~ 270|
|derivedCredentialProvider|[derivedCredentialProviderType](../resources/intune-deviceconfig-derivedcredentialprovidertype.md)|このアカウントに使用する派生資格情報プロバイダー。 可能な値は、`notConfigured`、`entrustDataCard`、`purebred`、`xTec`、`intercede` です。|
|derivedCredentialUrl|String|派生資格情報プロバイダーセルフサービス URI。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementSettings",
  "deviceComplianceCheckinThresholdDays": 1024,
  "isScheduledActionEnabled": true,
  "secureByDefault": true,
  "enhancedJailBreak": true,
  "deviceInactivityBeforeRetirementInDay": 1024,
  "derivedCredentialProvider": "String",
  "derivedCredentialUrl": "String"
}
```





