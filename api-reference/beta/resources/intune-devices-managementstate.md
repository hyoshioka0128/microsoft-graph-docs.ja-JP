---
title: managementState 列挙型
description: Microsoft Intune でのデバイスの管理状態。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 316e4d2ce97311e1a45f3324f2636054afd62664
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34963934"
---
# <a name="managementstate-enum-type"></a>managementState 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Microsoft Intune でのデバイスの管理状態。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|対象|.0|デバイスが管理下にある|
|retirePending|1-d|廃棄コマンドは、デバイス上および管理からの登録取り消しプロセス中に発生します。|
|retireFailed|pbm-2|デバイスでのリタイアコマンドが失敗しました|
|wipePending|1/3|ワイプコマンドがデバイス上で発生していて、管理からの登録取り消しプロセスである|
|wipeFailed|2/4|デバイスでワイプコマンドが失敗しました|
|正常|5|デバイスに問題があります。|
|deletePending|シックス|デバイスで削除コマンドが発生しています |
|retireIssued|7|デバイスに対して、廃棄コマンドが発行されました|
|wipeIssued 済み|8 |デバイスに対してワイプコマンドが発行されました|
|wipeCanceled|9 |このデバイスのワイプコマンドは取り消されました|
|retireCanceled|10 |このデバイスの廃棄コマンドは取り消されました|
|た|#|デバイスが検出されますが、完全に登録されていません。|





