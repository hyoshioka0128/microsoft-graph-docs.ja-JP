---
title: proxiedDomain リソースの種類
description: プロキシ化されたドメイン
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 9260d0fc9b446e7f61bfebff577ac10f9f3e4aee
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34986404"
---
# <a name="proxieddomain-resource-type"></a>proxiedDomain リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

プロキシ化されたドメイン

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|ipAddressOrFQDN|文字列|IP アドレスまたは FQDN|
|プロキシ|文字列|プロキシ IP または FQDN|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.proxiedDomain"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.proxiedDomain",
  "ipAddressOrFQDN": "String",
  "proxy": "String"
}
```





