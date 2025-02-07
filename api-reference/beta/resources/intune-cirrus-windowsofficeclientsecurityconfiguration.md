---
title: windowsOfficeClientSecurityConfiguration リソースの種類
description: まだ文書化されていません
localization_priority: Normal
author: rolyon
ms.prod: Intune
ms.openlocfilehash: 3e83afe7eb2dc06e6f9c8b2d94bdca4e414c2892
ms.sourcegitcommit: 94aaf594c881c02f353c6a417460cdf783a0bfe0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2019
ms.locfileid: "33949242"
---
# <a name="windowsofficeclientsecurityconfiguration-resource-type"></a>windowsOfficeClientSecurityConfiguration リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

まだ文書化されていません

[OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト windowsOfficeClientSecurityConfigurations](../api/intune-cirrus-windowsofficeclientsecurityconfiguration-list.md)|[windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)コレクション|[WindowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[WindowsOfficeClientSecurityConfiguration を取得する](../api/intune-cirrus-windowsofficeclientsecurityconfiguration-get.md)|[windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)|[WindowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[WindowsOfficeClientSecurityConfiguration を作成する](../api/intune-cirrus-windowsofficeclientsecurityconfiguration-create.md)|[windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)|新しい[windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)オブジェクトを作成します。|
|[WindowsOfficeClientSecurityConfiguration の削除](../api/intune-cirrus-windowsofficeclientsecurityconfiguration-delete.md)|None|[WindowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)を削除します。|
|[WindowsOfficeClientSecurityConfiguration の更新](../api/intune-cirrus-windowsofficeclientsecurityconfiguration-update.md)|[windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)|[WindowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|種類|説明|
|:---|:---|:---|
|id|文字列|Office クライアント構成ポリシーの Id。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|userPreferencePayload|Stream|プリファレンス設定 JSON 文字列はバイナリ形式です。これらの値はユーザーが上書きできます。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|policyPayload|Stream|ポリシー設定 JSON 文字列 (バイナリ形式) では、ユーザーがこれらの値を変更することはできません。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|description|String|管理者が提供する office クライアント構成ポリシーの説明。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|displayName|String|管理者が指定した office クライアント構成ポリシーの名前。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|priority|Int32|優先度の値は、テナントの各ポリシーの一意の値である必要があり、競合の解決に使用されます。低い値は、優先度が高くなります。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|lastModifiedDateTime|DateTime|ポリシーの最終更新日時スタンプ。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|userCheckinSummary|[officeUserCheckinSummary](../resources/intune-cirrus-officeusercheckinsummary.md)|ポリシーのユーザーチェックインの概要。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|checkinStatuses|[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)コレクション|Office クライアントのチェックイン状態のリスト。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|

## <a name="relationships"></a>関係
|リレーションシップ|型|説明|
|:---|:---|:---|
|assignments|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)コレクション|ポリシーのグループの割り当てのリスト。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsOfficeClientSecurityConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsOfficeClientSecurityConfiguration",
  "id": "String (identifier)",
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "String",
  "displayName": "String",
  "priority": 1024,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 1024,
    "failedUserCount": 1024
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "String",
      "deviceName": "String",
      "devicePlatform": "String",
      "devicePlatformVersion": "String",
      "wasSuccessful": true,
      "userId": "String",
      "checkinDateTime": "String (timestamp)",
      "errorMessage": "String",
      "appliedPolicies": [
        "String"
      ]
    }
  ]
}
```



