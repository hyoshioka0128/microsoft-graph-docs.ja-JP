---
title: windowsUniversalAppXContainedApp リソースの種類
description: WindowsUniversalAppX アプリの含まれているアプリを表すクラス。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 0345f8f6a2c5872e339d2ad69863e5c12677d861
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34985662"
---
# <a name="windowsuniversalappxcontainedapp-resource-type"></a>windowsUniversalAppXContainedApp リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

WindowsUniversalAppX アプリの含まれているアプリを表すクラス。


[MobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)から継承します。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト windowsUniversalAppXContainedApps](../api/intune-apps-windowsuniversalappxcontainedapp-list.md)|[windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)コレクション|[WindowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[WindowsUniversalAppXContainedApp を取得する](../api/intune-apps-windowsuniversalappxcontainedapp-get.md)|[windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)|[WindowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[WindowsUniversalAppXContainedApp を作成する](../api/intune-apps-windowsuniversalappxcontainedapp-create.md)|[windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)|新しい[windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)オブジェクトを作成します。|
|[WindowsUniversalAppXContainedApp の削除](../api/intune-apps-windowsuniversalappxcontainedapp-delete.md)|None|[WindowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)を削除します。|
|[WindowsUniversalAppXContainedApp の更新](../api/intune-apps-windowsuniversalappxcontainedapp-update.md)|[windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)|[WindowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティのキー。 [MobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)から継承します。|
|appUserModelId|String|WindowsUniversalAppX アプリの含まれているアプリのアプリユーザーモデル ID。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsUniversalAppXContainedApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUniversalAppXContainedApp",
  "id": "String (identifier)",
  "appUserModelId": "String"
}
```





