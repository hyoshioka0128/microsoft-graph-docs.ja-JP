---
title: Create vppToken
description: 新規にvppTokenオブジェクトを作成します。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 713a6bf583ff9c315ec88a83811312e6a6af5d92
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32582550"
---
# <a name="create-vpptoken"></a>Create vppToken

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

新規に[vppToken](../resources/intune-onboarding-vpptoken.md)オブジェクトを作成します。

## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementServiceConfig.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/vppTokens
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、vppToken オブジェクトの JSON 表記を指定します。

次の表に、vppToken 作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|appleVolumePurchaseProgramToken 作成時に自動的に生成されます。 エンティティのキーになります。|
|organizationName|String|Apple ボリューム購入プログラムのトークンに関連付けられている組織|
|vppTokenAccountType|[vppTokenAccountType](../resources/intune-shared-vpptokenaccounttype.md)|特定の Apple ボリューム購入プログラムのトークンが関連付けられている、ボリューム購入プログラムの種類。 可能な値は、`business`、`education` です。 可能な値は、`business`、`education` です。|
|appleId|String|特定の Apple ボリューム購入プログラムのトークンに関連付けられている Apple ID。|
|expirationDateTime|DateTimeOffset|Apple ボリューム購入プログラムのトークンの有効期限。|
|lastSyncDateTime|DateTimeOffset|Apple ボリューム購入プログラムのトークンを使用して、Apple ボリューム購入プログラム サービスと最後にアプリケーションの同期を行った日時。|
|token|String|Apple ボリューム購入プログラムからダウンロードした Apple ボリューム購入プログラムのトークン文字列。|
|lastModifiedDateTime|DateTimeOffset|Apple ボリューム購入プログラムのトークンに関連付けられている最終変更日時。|
|state|[vpptokenstate](../resources/intune-onboarding-vpptokenstate.md)|Apple ボリューム購入プログラムのトークンの現在の状態。 可能な値は、`unknown`、`valid`、`expired`、`invalid`、`assignedToExternalMDM` です。 可能な値は、`unknown`、`valid`、`expired`、`invalid`、`assignedToExternalMDM` です。|
|lastSyncStatus|[vpptokensyncstatus](../resources/intune-onboarding-vpptokensyncstatus.md)|Apple ボリューム購入プログラム トークンを使用して行われた最後のアプリケーションの同期の現在の同期状態。 可能な値は、`none`、`inProgress`、`completed`、`failed` です。 可能な値は、`none`、`inProgress`、`completed`、`failed` です。|
|automaticallyUpdateApps|Boolean|VPP トークンのアプリを自動で更新するかどうか。|
|countryOrRegion|文字列|VPP トークンのアプリを自動で更新するかどうか。|



## <a name="response"></a>応答
成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [vppToken](../resources/intune-onboarding-vpptoken.md) オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/vppTokens
Content-type: application/json
Content-length: 461

{
  "@odata.type": "#microsoft.graph.vppToken",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "state": "valid",
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value"
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 574

{
  "@odata.type": "#microsoft.graph.vppToken",
  "id": "9ceb2f92-2f92-9ceb-922f-eb9c922feb9c",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value"
}
```



