---
title: bitLockerRecoveryOptions リソースの種類
description: BitLocker 回復オプション。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: bf88795ac9f2708bc03607bc5d48d5ec69a822eb
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34991052"
---
# <a name="bitlockerrecoveryoptions-resource-type"></a>bitLockerRecoveryOptions リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

BitLocker 回復オプション。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|blockDataRecoveryAgent|Boolean|証明書ベースのデータ回復エージェントをブロックするかどうかを示します。|
|回復した Ypasswordusage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|ユーザーが固定またはシステムディスク用に48桁の回復パスワードを生成することを許可または要求するかどうかを示します。 可能な値は、`blocked`、`required`、`allowed` です。|
|recoveryKeyUsage|[configurationUsage](../resources/intune-deviceconfig-configurationusage.md)|ユーザーが固定またはシステムディスクの256ビット回復キーを生成することを許可または要求するかどうかを示します。 可能な値は、`blocked`、`required`、`allowed` です。|
|hideRecoveryOptions|Boolean|固定またはシステムディスクの BitLocker セットアップウィザードでの復元オプションの表示を許可するかどうかを示します。|
|enableRecoveryInformationSaveToStore|Boolean|AD DS に BitLocker 回復情報を格納することを許可するかどうかを示します。|
|recoveryInformationToStore|[bitLockerRecoveryInformationType](../resources/intune-deviceconfig-bitlockerrecoveryinformationtype.md)|AD DS に格納される BitLocker 回復情報の種類を構成します。 可能な値は、`passwordAndKey`、`passwordOnly` です。|
|enableBitLockerAfterRecoveryInformationToStore|Boolean|AD DS に回復情報が格納されるまで BitLocker を有効にするかどうかを示します。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerRecoveryOptions"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerRecoveryOptions",
  "blockDataRecoveryAgent": true,
  "recoveryPasswordUsage": "String",
  "recoveryKeyUsage": "String",
  "hideRecoveryOptions": true,
  "enableRecoveryInformationSaveToStore": true,
  "recoveryInformationToStore": "String",
  "enableBitLockerAfterRecoveryInformationToStore": true
}
```





