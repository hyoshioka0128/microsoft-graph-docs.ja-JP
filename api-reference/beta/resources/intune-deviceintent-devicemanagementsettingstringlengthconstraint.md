---
title: Devicemanagementsettingstringlength 制約リソースの種類
description: 指定した文字列の長さの範囲を適用する制約
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: d7cdcdeb138dce2c5b201527a079e3ee2de03737
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34984465"
---
# <a name="devicemanagementsettingstringlengthconstraint-resource-type"></a>Devicemanagementsettingstringlength 制約リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

指定した文字列の長さの範囲を適用する制約


[Devicemanagementconstraint](../resources/intune-deviceintent-devicemanagementconstraint.md)から継承します

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|minimumLength|Int32|許可される最小文字列の長さ|
|maximumLength|Int32|許可される最大文字列長|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementSettingStringLengthConstraint"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementSettingStringLengthConstraint",
  "minimumLength": 1024,
  "maximumLength": 1024
}
```





