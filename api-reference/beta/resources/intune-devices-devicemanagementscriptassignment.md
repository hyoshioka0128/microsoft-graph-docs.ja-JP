---
title: deviceManagementScriptAssignment リソースの種類
description: グループにデバイス管理スクリプトを割り当てるために使用されるプロパティが含まれています。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: b1f76f1cb230b20b01b66387bb1faed2b8a82f01
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34995344"
---
# <a name="devicemanagementscriptassignment-resource-type"></a>deviceManagementScriptAssignment リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

グループにデバイス管理スクリプトを割り当てるために使用されるプロパティが含まれています。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト deviceManagementScriptAssignments](../api/intune-devices-devicemanagementscriptassignment-list.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)コレクション|[DeviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[DeviceManagementScriptAssignment を取得する](../api/intune-devices-devicemanagementscriptassignment-get.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|[DeviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[DeviceManagementScriptAssignment を作成する](../api/intune-devices-devicemanagementscriptassignment-create.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|新しい[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトを作成します。|
|[DeviceManagementScriptAssignment の削除](../api/intune-devices-devicemanagementscriptassignment-delete.md)|None|[DeviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)を削除します。|
|[DeviceManagementScriptAssignment の更新](../api/intune-devices-devicemanagementscriptassignment-update.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|[DeviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|[デバイス管理スクリプト] グループ割り当てエンティティのキー。|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|スクリプトを対象としている Azure Active Directory グループの Id。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





