---
title: win32LobAppRegistryDetectionType 列挙型
description: サポートされているすべてのレジストリデータ検出の種類が含まれます。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: ac32e469332c1f28537b904f4d6b5992c7871e7d
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34986089"
---
# <a name="win32lobappregistrydetectiontype-enum-type"></a>win32LobAppRegistryDetectionType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

サポートされているすべてのレジストリデータ検出の種類が含まれます。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|notConfigured|.0|構成されていません。|
|ある|1-d|指定されたレジストリキーまたは値が存在します。|
|doesNotExist|pbm-2|指定したレジストリキーまたは値が存在しません。|
|string|1/3|文字列型 (String) の値を指定します。|
|整数|2/4|整数型 (Integer) の値です。|
|バージョン|5|バージョン値の種類。|





