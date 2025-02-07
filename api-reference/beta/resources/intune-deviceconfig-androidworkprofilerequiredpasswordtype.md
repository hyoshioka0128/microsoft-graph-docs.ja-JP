---
title: androidWorkProfileRequiredPasswordType 列挙型
description: Android の作業プロファイルに必要なパスワードの種類。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: c1ebbbb51390d5d96afcfe0e2d4805e0ba9a3007
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34993775"
---
# <a name="androidworkprofilerequiredpasswordtype-enum-type"></a>androidWorkProfileRequiredPasswordType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android の作業プロファイルに必要なパスワードの種類。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|deviceDefault|.0|デバイスの既定値。意図的ではありません。|
|lowSecurityBiometric 認証|1-d|低セキュリティ生体認証ベースのパスワードが必要です。|
|必須|pbm-2|必須です。|
|atLeastNumeric|1/3|少なくとも数値のパスワードが必要です。|
|numericComplex|2/4|数字の複雑なパスワードが必要です。|
|Atall Stアルファベット|5|少なくとも英字のパスワードが必要です。|
|atLeastAlphanumeric|シックス|少なくとも英数字のパスワードが必要です。|
|alphanumericWithSymbols|7|記号パスワードが必要な、少なくとも英数字。|





