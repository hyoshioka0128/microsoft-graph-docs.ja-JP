---
title: embeddedSIMActivationCode リソースの種類
description: 携帯電話会社から提供された、埋め込まれた SIM ライセンス認証コード。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: c96bc6530de0e8e6d1fde95fa71ffb6f1bdedb18
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34994882"
---
# <a name="embeddedsimactivationcode-resource-type"></a>embeddedSIMActivationCode リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

携帯電話会社から提供された、埋め込まれた SIM ライセンス認証コード。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|integratedCircuitCardIdentifier|String|携帯電話会社が提供する、この組み込み SIM アクティブ化コードの Ic カード識別子 (ICCID)。
入力は、次の正規表現に一致して\[いる\]{19}\[必要\]があります: ' ^ 0-9 0-9? $ '。|
|matchingIdentifier|String|GSMA Association MatchingIdentifier (MatchingID) セクション4.1 で指定されているように、()。
入力は、次の正規表現に一致する必要\[があります: ' ^ ZA\-\]-Z0-9 * $ '。|
|smdpPlusServerAddress|String|GSM Association SPG .22 RSP Technical 仕様で指定されているとおりに、SM-DP + サーバーの完全修飾ドメイン名。
入力は、次の正規表現に一致している\[必要があります: ' ^\](zA-\[Z0-\]9 +)\.*) +\[a-zA-Z\]{2,}$ '。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.embeddedSIMActivationCode"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCode",
  "integratedCircuitCardIdentifier": "String",
  "matchingIdentifier": "String",
  "smdpPlusServerAddress": "String"
}
```





