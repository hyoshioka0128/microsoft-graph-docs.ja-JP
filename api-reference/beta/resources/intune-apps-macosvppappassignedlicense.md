---
title: macOsVppAppAssignedLicense リソースの種類
description: MacOS ボリューム購入プログラムのライセンス割り当てです。 このクラスは、作成、削除、更新をサポートしていません。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: ce80e1283354e69bae6b0a0a0f3cc34ff67bf4e7
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34989169"
---
# <a name="macosvppappassignedlicense-resource-type"></a>macOsVppAppAssignedLicense リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

MacOS ボリューム購入プログラムのライセンス割り当てです。 このクラスは、作成、削除、更新をサポートしていません。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト macOsVppAppAssignedLicenses](../api/intune-apps-macosvppappassignedlicense-list.md)|[macOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)コレクション|[MacOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[MacOsVppAppAssignedLicense を取得する](../api/intune-apps-macosvppappassignedlicense-get.md)|[macOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)|[MacOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[MacOsVppAppAssignedLicense を作成する](../api/intune-apps-macosvppappassignedlicense-create.md)|[macOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)|新しい[macOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)オブジェクトを作成します。|
|[MacOsVppAppAssignedLicense の削除](../api/intune-apps-macosvppappassignedlicense-delete.md)|None|[MacOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)を削除します。|
|[MacOsVppAppAssignedLicense の更新](../api/intune-apps-macosvppappassignedlicense-update.md)|[macOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)|[MacOsVppAppAssignedLicense](../resources/intune-apps-macosvppappassignedlicense.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|エンティティのキー。|
|userEmailAddress|String|ユーザーの電子メールアドレス。|
|userId|String|ユーザー ID。|
|userName|String|ユーザー名。|
|userPrincipalName|String|ユーザー プリンシパル名。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.macOsVppAppAssignedLicense"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOsVppAppAssignedLicense",
  "id": "String (identifier)",
  "userEmailAddress": "String",
  "userId": "String",
  "userName": "String",
  "userPrincipalName": "String"
}
```





