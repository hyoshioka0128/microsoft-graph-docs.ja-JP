---
title: officeClientConfigurationAssignment リソースの種類
description: Office クライアントの構成の割り当て。
localization_priority: Normal
author: rolyon
ms.prod: Intune
ms.openlocfilehash: 7c222d16166d9dc63500a970d378ff0d28271eed
ms.sourcegitcommit: 94aaf594c881c02f353c6a417460cdf783a0bfe0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2019
ms.locfileid: "33949256"
---
# <a name="officeclientconfigurationassignment-resource-type"></a>officeClientConfigurationAssignment リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Office クライアントの構成の割り当て。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト officeClientConfigurationAssignments](../api/intune-cirrus-officeclientconfigurationassignment-list.md)|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)コレクション|[OfficeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[OfficeClientConfigurationAssignment を取得する](../api/intune-cirrus-officeclientconfigurationassignment-get.md)|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)|[OfficeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[OfficeClientConfigurationAssignment を作成する](../api/intune-cirrus-officeclientconfigurationassignment-create.md)|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)|新しい[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)オブジェクトを作成します。|
|[OfficeClientConfigurationAssignment の削除](../api/intune-cirrus-officeclientconfigurationassignment-delete.md)|None|[OfficeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)を削除します。|
|[OfficeClientConfigurationAssignment の更新](../api/intune-cirrus-officeclientconfigurationassignment-update.md)|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)|[OfficeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|OfficeConfigurationAssignment の Id。|
|target|[officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)|管理者によって定義されたターゲットの割り当て。|

## <a name="relationships"></a>関係
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeClientConfigurationAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeClientConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
  }
}
```



