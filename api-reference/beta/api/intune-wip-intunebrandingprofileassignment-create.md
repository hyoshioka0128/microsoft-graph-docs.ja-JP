---
title: IntuneBrandingProfileAssignment を作成する
description: 新しい intuneBrandingProfileAssignment オブジェクトを作成します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 51797d3b65f4ae232919f79cd37d21360052ee7a
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34990580"
---
# <a name="create-intunebrandingprofileassignment"></a>IntuneBrandingProfileAssignment を作成する

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

新しい[intuneBrandingProfileAssignment](../resources/intune-wip-intunebrandingprofileassignment.md)オブジェクトを作成します。

## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementApps.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}/assignments
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、intuneBrandingProfileAssignment オブジェクトの JSON 表記を指定します。

次の表に、intuneBrandingProfileAssignment の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティの一意識別子。|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|ブランド化プロファイルが割り当てられている割り当て先。|



## <a name="response"></a>応答
成功した場合、このメソッド`201 Created`は応答コードと、応答本文で[intuneBrandingProfileAssignment](../resources/intune-wip-intunebrandingprofileassignment.md)オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/beta/deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}/assignments
Content-type: application/json
Content-length: 171

{
  "@odata.type": "#microsoft.graph.intuneBrandingProfileAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 220

{
  "@odata.type": "#microsoft.graph.intuneBrandingProfileAssignment",
  "id": "ee38a117-a117-ee38-17a1-38ee17a138ee",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





