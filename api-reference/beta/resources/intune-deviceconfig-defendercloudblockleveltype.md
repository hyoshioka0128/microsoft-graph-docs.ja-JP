---
title: defenderCloudBlockLevelType 列挙型
description: クラウドブロックレベルの可能な値
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 3f798e4b7572cc2593d0d742ecbdebf81d65507d
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34979866"
---
# <a name="defendercloudblockleveltype-enum-type"></a>defenderCloudBlockLevelType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

クラウドブロックレベルの可能な値

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|notConfigured|.0|既定値は、Windows Defender ウイルス対策の既定のブロックレベルを使用し、正当なファイルを検出するリスクを増やさずに、強力な検出を提供します。|
|高額|1-d|High は、強力なレベルの検出を適用します。|
|highPlus|pbm-2|高 + は高レベルを使用し、追加の保護対策を適用します。|
|zeroTolerance|1/3|ゼロトレランスによってすべての不明な実行可能ファイルがブロック|





