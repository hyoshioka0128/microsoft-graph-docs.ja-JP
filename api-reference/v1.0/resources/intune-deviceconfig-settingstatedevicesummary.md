---
title: settingStateDeviceSummary リソースの種類
description: 設定状態の要約に対する、デバイス コンプライアンス ポリシーおよび構成
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 429ee25a57383b7356948242ce39dcb45b4067ba
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32534746"
---
# <a name="settingstatedevicesummary-resource-type"></a>settingStateDeviceSummary リソースの種類

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

設定状態の要約に対する、デバイス コンプライアンス ポリシーおよび構成

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[settingStateDeviceSummaries のリスト](../api/intune-deviceconfig-settingstatedevicesummary-list.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) コレクション|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[settingStateDeviceSummary の取得](../api/intune-deviceconfig-settingstatedevicesummary-get.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[settingStateDeviceSummary の作成](../api/intune-deviceconfig-settingstatedevicesummary-create.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|新しい [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) オブジェクトを作成します。|
|[settingStateDeviceSummary の削除](../api/intune-deviceconfig-settingstatedevicesummary-delete.md)|なし|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) を削除します。|
|[settingStateDeviceSummary の更新](../api/intune-deviceconfig-settingstatedevicesummary-update.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティのキー。|
|settingName|文字列型 (String)|設定の名前|
|instancePath|String|設定の InstancePath の名前|
|unknownDeviceCount|Int32|設定の不明なデバイスの数|
|notApplicableDeviceCount|Int32|設定の該当しないデバイスの数|
|compliantDeviceCount|Int32|設定の準拠しているデバイスの数|
|remediatedDeviceCount|Int32|設定の準拠しているデバイスの数|
|nonCompliantDeviceCount|Int32|設定の準拠していないデバイスの数|
|errorDeviceCount|Int32|設定のデバイス エラーの数|
|conflictDeviceCount|Int32|設定のデバイス競合エラーの数|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.settingStateDeviceSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
  "id": "String (identifier)",
  "settingName": "String",
  "instancePath": "String",
  "unknownDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "conflictDeviceCount": 1024
}
```



