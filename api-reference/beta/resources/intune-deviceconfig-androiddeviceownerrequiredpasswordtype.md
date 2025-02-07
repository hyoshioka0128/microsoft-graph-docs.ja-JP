---
title: androidDeviceOwnerRequiredPasswordType 列挙型
description: Android デバイスの所有者ポリシーに必要なパスワードの種類。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: e55aa24896e72a2351cfbfc2ac8a88ac2a2d3dd8
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34983793"
---
# <a name="androiddeviceownerrequiredpasswordtype-enum-type"></a>androidDeviceOwnerRequiredPasswordType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android デバイスの所有者ポリシーに必要なパスワードの種類。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|deviceDefault|.0|デバイスの既定値。意図的ではありません。|
|必須|1-d|パスワードを設定する必要がありますが、種類に制限はありません。|
|数値|pbm-2|少なくとも数値。|
|numericComplex|1/3|繰り返しまたは順序付けられていない、少なくとも数値。|
|読み|2/4|少なくとも英字のパスワード。|
|文字|5|少なくとも英数字のパスワード|
|alphanumericWithSymbols|シックス|記号を含む、少なくとも英数字。|
|lowSecurityBiometric 認証|7|低セキュリティ生体認証ベースのパスワードが必要です。|





