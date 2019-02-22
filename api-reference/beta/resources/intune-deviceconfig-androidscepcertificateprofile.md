---
title: androidScepCertificateProfile リソースの種類
description: Android SCEP 証明書のプロファイル
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: c2e61a1cffd3518720b3a46f89f46e543659d6de
ms.sourcegitcommit: 03421b75d717101a499e0b311890f5714056e29e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "30148329"
---
# <a name="androidscepcertificateprofile-resource-type"></a>androidScepCertificateProfile リソースの種類

> **重要:** ベータ版の Microsoft Graph api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android SCEP 証明書のプロファイル


[androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト androidScepCertificateProfiles](../api/intune-deviceconfig-androidscepcertificateprofile-list.md)|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)コレクション|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[androidScepCertificateProfile を取得する](../api/intune-deviceconfig-androidscepcertificateprofile-get.md)|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[androidScepCertificateProfile を作成する](../api/intune-deviceconfig-androidscepcertificateprofile-create.md)|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)|新しい[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)オブジェクトを作成します。|
|[androidScepCertificateProfile の削除](../api/intune-deviceconfig-androidscepcertificateprofile-delete.md)|なし|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)を削除します。|
|[androidScepCertificateProfile の更新](../api/intune-deviceconfig-androidscepcertificateprofile-update.md)|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)|[androidScepCertificateProfile](../resources/intune-deviceconfig-androidscepcertificateprofile.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|エンティティのキー。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|オブジェクトが最後に変更された DateTime。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|roleScopeTagIds|String collection|このエンティティインスタンスの範囲タグのリスト。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|supportsScopeTags|ブール値|基になるデバイス構成がスコープタグの割り当てをサポートしているかどうかを示します。 この値が false である場合、ScopeTags プロパティへの割り当ては許可されません。エンティティは、スコープを持つユーザーには表示されません。 これは Silverlight で作成された従来のポリシーに対して実行され、Azure ポータルでポリシーを削除して再作成することによって解決できます。 このプロパティは読み取りのみ可能です。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|createdDateTime|DateTimeOffset|オブジェクトが作成された DateTime。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|説明|String|デバイス構成について管理者が提供した説明。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|displayName|String|デバイス構成について管理者が指定した名前。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|version|Int32|デバイス構成のバージョン。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|renewalThresholdPercentage|Int32|証明書の更新しきい値の割合。 [androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承される有効な値は1から99。|
|subjectNameFormat|[subjectNameFormat](../resources/intune-deviceconfig-subjectnameformat.md)|証明書のサブジェクト名の形式。 [androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承します。 可能な値は、`commonName`、`commonNameIncludingEmail`、`commonNameAsEmail`、`custom`、`commonNameAsIMEI`、`commonNameAsSerialNumber`、`commonNameAsAadDeviceId`、`commonNameAsIntuneDeviceId`、`commonNameAsDurableDeviceId` です。|
|subjectAlternativeNameType|[subjectAlternativeNameType](../resources/intune-deviceconfig-subjectalternativenametype.md)|証明書のサブジェクトの別名の種類。 [androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承します。 可能な値は、`none`、`emailAddress`、`userPrincipalName`、`customAzureADAttribute`、`domainNameService` です。|
|certificateValidityPeriodValue|Int32|証明書の有効期間の値。 [androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承します|
|certificateValidityPeriodScale|[certificateValidityPeriodScale](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|証明書の有効期間のスケール。 [androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承します。 可能な値は `days`、`months`、`years` です。|
|extendedkeyusages|[extendedkeyusage](../resources/intune-deviceconfig-extendedkeyusage.md)コレクション|拡張キー使用法 (EKU) の設定。 このコレクションには、最大で 500 個の要素を含めることができます。 [androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承します|
|scepServerUrls|String collection|SCEP サーバーの Url|
|subjectnameformatstring プロパティ|String|SubjectNameFormat = custom で使用するカスタム形式。 例: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = エンタープライズユーザー, O = Contoso Corporation, L = Redmond, ST = WA, C = US|
|keyusage|[keyusages](../resources/intune-deviceconfig-keyusages.md)|SCEP キーの使用法。 使用可能な値は、`keyEncipherment`、`digitalSignature` です。|
|keySize|[keySize](../resources/intune-deviceconfig-keysize.md)|SCEP キーのサイズ。 使用可能な値は、`size1024`、`size2048` です。|
|hashAlgorithm|[hashalgorithms](../resources/intune-deviceconfig-hashalgorithms.md)|SCEP ハッシュアルゴリズム。 使用可能な値は、`sha1`、`sha2` です。|
|subjectAlternativeNameFormatString|String|AAD 属性を定義するカスタム文字列。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|groupAssignments|[deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)コレクション|デバイスの構成プロファイルのグループ割り当てのリストです。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|assignments|[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) コレクション|デバイスの構成プロファイルの割り当てのリスト。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|deviceStatuses|[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) コレクション|デバイスごとのデバイス構成のインストール状況。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|userStatuses|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) コレクション|ユーザーごとのデバイス構成のインストール状態。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|デバイス構成のデバイス状態の概要 ([deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|デバイス構成のユーザー状態の概要 ([deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承)|
|deviceSettingStateSummaries|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) コレクション|デバイス構成設定状態のデバイスの要約 ([deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承)|
|rootcertificate|[androidtrustedrootcertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md)|信頼されたルート証明書。 [androidcertificateprofilebase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)から継承します|
|managedDeviceCertificateStates|[managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md)コレクション|デバイスの証明書の状態|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidScepCertificateProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidScepCertificateProfile",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "renewalThresholdPercentage": 1024,
  "subjectNameFormat": "String",
  "subjectAlternativeNameType": "String",
  "certificateValidityPeriodValue": 1024,
  "certificateValidityPeriodScale": "String",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "String",
      "objectIdentifier": "String"
    }
  ],
  "scepServerUrls": [
    "String"
  ],
  "subjectNameFormatString": "String",
  "keyUsage": "String",
  "keySize": "String",
  "hashAlgorithm": "String",
  "subjectAlternativeNameFormatString": "String"
}
```




