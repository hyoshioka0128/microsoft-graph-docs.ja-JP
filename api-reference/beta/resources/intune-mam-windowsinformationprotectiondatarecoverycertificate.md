---
title: windowsInformationProtectionDataRecoveryCertificate リソースの種類
description: Windows 情報保護の DataRecoveryCertificate
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 32a18b25209301e3aeb62aaeaf63f080955cf669
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34994532"
---
# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a>windowsInformationProtectionDataRecoveryCertificate リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Windows 情報保護の DataRecoveryCertificate

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|subjectName|文字列型 (String)|データ回復証明書のサブジェクト名|
|description|String|データ回復証明書の説明|
|expirationDateTime|DateTimeOffset|データ回復証明書の有効期限日時|
|certificate|バイナリ型 (Binary)|データ回復証明書|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
  "subjectName": "String",
  "description": "String",
  "expirationDateTime": "String (timestamp)",
  "certificate": "binary"
}
```





