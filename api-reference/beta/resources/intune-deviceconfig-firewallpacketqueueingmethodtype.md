---
title: firewallPacketQueueingMethodType 列挙型
description: FirewallPacketQueueingMethod に指定できる値
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: a4c7556fb3c37f9bfd564e31744f0e27a4482d6e
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34985851"
---
# <a name="firewallpacketqueueingmethodtype-enum-type"></a>firewallPacketQueueingMethodType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

FirewallPacketQueueingMethod に指定できる値

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|deviceDefault|.0|Intune によって構成された値がない。ユーザーが構成したデバイスの既定値を上書きしない|
|党|1-d|パケットキューを無効にする|
|queueInbound|pbm-2|暗号化された着信パケットをキューに保存する|
|queueOutbound|1/3|転送のためにキューに復号化された送信パケット|
|queueBoth|2/4|受信パケットと送信パケットの両方をキューにする|





