---
title: androidPermissionAction リソースの種類
description: Android アプリのアクセス許可と Android のアクションとの間のマッピングは、そのアクセス許可が要求されたときに行われる必要があります。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 5237cc214ed6e5d7319d947b308cc666337e6d1b
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34991290"
---
# <a name="androidpermissionaction-resource-type"></a>androidPermissionAction リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android アプリのアクセス許可と Android のアクションとの間のマッピングは、そのアクセス許可が要求されたときに行われる必要があります。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|権|String|Android のアクセス許可文字列。公式の Android ドキュメントで定義されています。  例 ' READ_CONTACTS '。|
|action|[androidPermissionActionType](../resources/intune-apps-androidpermissionactiontype.md)|Android のアクセス許可アクションの種類。 可能な値は、`prompt`、`autoGrant`、`autoDeny` です。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidPermissionAction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidPermissionAction",
  "permission": "String",
  "action": "String"
}
```





