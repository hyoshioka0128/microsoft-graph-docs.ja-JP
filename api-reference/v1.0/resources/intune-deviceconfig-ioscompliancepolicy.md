---
title: iosCompliancePolicy リソースの種類
description: このクラスには、iOS のコンプライアンス設定が含まれています。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: b63f77acd121ea6fe3499686b2c7c6144aa26d95
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32580996"
---
# <a name="ioscompliancepolicy-resource-type"></a>iosCompliancePolicy リソースの種類

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

このクラスには、iOS のコンプライアンス設定が含まれています。


[deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[iosCompliancePolicies のリスト](../api/intune-deviceconfig-ioscompliancepolicy-list.md)|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) コレクション|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[iosCompliancePolicy の取得](../api/intune-deviceconfig-ioscompliancepolicy-get.md)|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md)|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[iosCompliancePolicy の作成](../api/intune-deviceconfig-ioscompliancepolicy-create.md)|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md)|新しい [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) オブジェクトを作成します。|
|[iosCompliancePolicy の削除](../api/intune-deviceconfig-ioscompliancepolicy-delete.md)|なし|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) を削除します。|
|[iosCompliancePolicy の更新](../api/intune-deviceconfig-ioscompliancepolicy-update.md)|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md)|[iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列型 (String)|エンティティのキー。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|createdDateTime|DateTimeOffset|オブジェクトが作成された DateTime。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|説明|String|管理者が指定した、デバイス構成についての説明。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|オブジェクトの最終更新の DateTime。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|displayName|String|管理者が指定した、デバイス構成の名前。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|version|Int32|デバイス構成のバージョン。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|passcodeBlockSimple|Boolean|単純なパスコードを禁止するかどうかを示します。|
|passcodeExpirationDays|Int32|パスコードの有効期限が切れるまでの日数。 有効な値は 1 から 65535 までです|
|passcodeMinimumLength|Int32|パスコードの最小の長さ。 有効な値は 4 から 14 までです|
|passcodeMinutesOfInactivityBeforeLock|Int32|パスコードが要求されるまでの非アクティブ時間 (分)。|
|passcodePreviousPasscodeBlockCount|Int32|ブロックする、以前のパスコードの数。 有効な値は 1 から 24 までです|
|passcodeMinimumCharacterSetCount|Int32|パスワードに必要な文字セットの数。|
|passcodeRequiredType|[requiredpasswordtype](../resources/intune-deviceconfig-requiredpasswordtype.md)|必要なパスコードの種類。 可能な値は、`deviceDefault`、`alphanumeric`、`numeric` です。|
|passcodeRequired|Boolean|パスコードを要求するかどうかを指定します。|
|osMinimumVersion|String|最小の iOS バージョン。|
|osMaximumVersion|String|最大の iOS バージョン。|
|securityBlockJailbrokenDevices|Boolean|デバイスの脱獄またはルート化を認めません。|
|deviceThreatProtectionEnabled|Boolean|デバイスの脅威保護が有効になっている必要があります。|
|deviceThreatProtectionRequiredSecurityLevel|[deviceThreatProtectionLevel](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|Mobile Threat Protection に、コンプライアンス違反をレポートするための最小のリスク レベルを要求します。 可能な値は、`unavailable`、`secured`、`low`、`medium`、`high`、`notSet` です。|
|managedEmailProfileRequired|Boolean|管理された電子メール プロファイルを要求するかどうかを指定します。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|scheduledActionsForRule|[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) コレクション|このルールのスケジュール済みのアクションのリスト ([deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承)|
|deviceStatuses|[deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) コレクション|DeviceComplianceDeviceStatus のリストです。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|userStatuses|[deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) コレクション|DeviceComplianceUserStatus のリストです。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|
|deviceStatusOverview|[deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md)|デバイス コンプライアンスのデバイス状態の概要 ([deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承)|
|userStatusOverview|[deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md)|デバイス コンプライアンスのユーザー状態の概要 ([deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承)|
|deviceSettingStateSummaries|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) コレクション|コンプライアンス設定状態のデバイスの要約 ([deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承)|
|assignments|[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) コレクション|このコンプライアンス ポリシーの割り当てのコレクションです。 [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) から継承します|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 1024,
  "passcodeMinimumLength": 1024,
  "passcodeMinutesOfInactivityBeforeLock": 1024,
  "passcodePreviousPasscodeBlockCount": 1024,
  "passcodeMinimumCharacterSetCount": 1024,
  "passcodeRequiredType": "String",
  "passcodeRequired": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "String",
  "managedEmailProfileRequired": true
}
```



