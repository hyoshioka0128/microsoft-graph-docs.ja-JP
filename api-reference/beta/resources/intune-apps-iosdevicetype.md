---
title: iosDeviceType リソースの種類
description: モバイル アプリを実行できる iOS デバイスの種類のプロパティが含まれます。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: d9751d541b0bcb64b68673aa8ca646fb85e70b5f
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34991304"
---
# <a name="iosdevicetype-resource-type"></a>iosDeviceType リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

モバイル アプリを実行できる iOS デバイスの種類のプロパティが含まれます。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|iPad|Boolean|アプリを iPad で実行できるかどうか。|
|iPhoneAndIPod|ブール型 (Boolean)|アプリを iPhone および iPod で実行できるかどうか。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosDeviceType"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosDeviceType",
  "iPad": true,
  "iPhoneAndIPod": true
}
```





