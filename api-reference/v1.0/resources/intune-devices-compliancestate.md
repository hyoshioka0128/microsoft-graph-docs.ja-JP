---
title: complianceState 列挙型
description: コンプライアンスの状態です。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: d578417c616fc2dbf30b8fe95d2f58ede5fd3df2
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32568139"
---
# <a name="compliancestate-enum-type"></a>complianceState 列挙型

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

コンプライアンスの状態です。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|不明|.0|わかり.|
|要件|1 |要件.|
|互換性|2 |デバイスは非準拠で、企業リソースからブロックされます。|
|異なる|3 |他のルールと競合しています。|
|error|4 |Error。|
|inGracePeriod|254|デバイスは準拠していないが、会社のリソースにアクセスできる|
|configmanager|255|構成マネージャーによる管理|



