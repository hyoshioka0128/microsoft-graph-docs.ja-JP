---
title: deviceConfigurationSettingState リソースの種類
description: 指定されたデバイスのデバイス構成設定の状態。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: d79d4c35572c98c82f80f8903d42cfa3b983c2e9
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32573446"
---
# <a name="deviceconfigurationsettingstate-resource-type"></a>deviceConfigurationSettingState リソースの種類

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

指定されたデバイスのデバイス構成設定の状態。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|setting|String|レポートされる設定値。|
|settingName|String|レポートされている、ローカライズされた設定名またはユーザー フレンドリな設定名|
|instanceDisplayName|String|レポートされている設定インスタンスの名前です。|
|state|[complianceStatus](../resources/intune-shared-compliancestatus.md)|設定のコンプライアンス状態。 可能な値は、`unknown`、`notApplicable`、`compliant`、`remediated`、`nonCompliant`、`error`、`conflict`、`notAssigned` です。|
|errorCode|Int64|設定のエラー コード|
|errorDescription|String|エラーの説明|
|userId|String|UserId|
|userName|String|UserName|
|userEmail|String|UserEmail|
|userPrincipalName|String|UserPrincipalName。|
|sources|[settingSource](../resources/intune-deviceconfig-settingsource.md) コレクション|投稿ポリシー|
|currentValue|String|デバイスに関する設定の現在の値|

## <a name="relationships"></a>関係
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceConfigurationSettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationSettingState",
  "setting": "String",
  "settingName": "String",
  "instanceDisplayName": "String",
  "state": "String",
  "errorCode": 1024,
  "errorDescription": "String",
  "userId": "String",
  "userName": "String",
  "userEmail": "String",
  "userPrincipalName": "String",
  "sources": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "String",
      "displayName": "String"
    }
  ],
  "currentValue": "String"
}
```



