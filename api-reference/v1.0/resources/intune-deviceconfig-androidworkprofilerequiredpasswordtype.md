---
title: androidWorkProfileRequiredPasswordType 列挙型
description: Android の作業プロファイルに必要なパスワードの種類。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: b1dbb0b7e523ea6ca3ac1be3328cf58e30d9a892
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32575157"
---
# <a name="androidworkprofilerequiredpasswordtype-enum-type"></a>androidWorkProfileRequiredPasswordType 列挙型

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android の作業プロファイルに必要なパスワードの種類。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|devicedefault|.0|デバイスの既定値。意図的ではありません。|
|lowsecuritybiometric 認証|1 |低セキュリティ生体認証ベースのパスワードが必要です。|
|必須|2 |必須です。|
|atleastnumeric|3 |少なくとも数値のパスワードが必要です。|
|numericcomplex|4 |数字の複雑なパスワードが必要です。|
|atall stアルファベット|5 |少なくとも英字のパスワードが必要です。|
|atleastalphanumeric|6 |少なくとも英数字のパスワードが必要です。|
|alphanumericWithSymbols|7 |記号パスワードが必要な、少なくとも英数字。|



