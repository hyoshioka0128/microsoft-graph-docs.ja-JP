---
title: securityBaselineStateSummary リソースの種類
description: アカウントのセキュリティベースラインのセキュリティベースラインコンプライアンスの状態の要約。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: cd3ec6e2b207adc70fbcd6ea793a636a799bf1bc
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34983408"
---
# <a name="securitybaselinestatesummary-resource-type"></a>securityBaselineStateSummary リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

アカウントのセキュリティベースラインのセキュリティベースラインコンプライアンスの状態の要約。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[SecurityBaselineStateSummary を取得する](../api/intune-deviceintent-securitybaselinestatesummary-get.md)|[securityBaselineStateSummary](../resources/intune-deviceintent-securitybaselinestatesummary.md)|[SecurityBaselineStateSummary](../resources/intune-deviceintent-securitybaselinestatesummary.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[SecurityBaselineStateSummary の更新](../api/intune-deviceintent-securitybaselinestatesummary-update.md)|[securityBaselineStateSummary](../resources/intune-deviceintent-securitybaselinestatesummary.md)|[SecurityBaselineStateSummary](../resources/intune-deviceintent-securitybaselinestatesummary.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティの一意識別子。|
|secureCount|Int32|セキュリティで保護されたデバイスの数|
|notSecureCount|Int32|セキュリティで保護されていないデバイスの数|
|unknownCount|Int32|不明なデバイスの数|
|errorCount|Int32|エラー デバイスの数|
|conflictCount|Int32|競合デバイスの数|
|notApplicableCount|Int32|該当しないデバイスの数|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.securityBaselineStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.securityBaselineStateSummary",
  "id": "String (identifier)",
  "secureCount": 1024,
  "notSecureCount": 1024,
  "unknownCount": 1024,
  "errorCount": 1024,
  "conflictCount": 1024,
  "notApplicableCount": 1024
}
```





