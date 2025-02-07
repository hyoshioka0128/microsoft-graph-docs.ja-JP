---
title: VPPトークンの更新
description: VPPトークン オブジェクトのプロパティを更新します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: ea27c93b80c55bc7a86b8e4835fd562c855ecf1b
ms.sourcegitcommit: 121c0fad692fb3c5c01dc051481b5249e4491b48
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2019
ms.locfileid: "35620942"
---
# <a name="update-vpptoken"></a>VPPトークンの更新

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

[VPPトークン](../resources/intune-onboarding-vpptoken.md) オブジェクトのプロパティを更新します。

## <a name="prerequisites"></a>必要条件
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
PATCH /deviceAppManagement/vppTokens/{vppTokenId}
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、[VPPトークン](../resources/intune-onboarding-vpptoken.md) オブジェクトの JSON 表記を指定します。

次の表に、[VPPトークン](../resources/intune-onboarding-vpptoken.md) の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|appleVolumePurchaseProgramToken 作成時に自動的に生成されます。 エンティティのキーになります。|
|organizationName|String|Apple ボリューム購入プログラムのトークンに関連付けられている組織|
|vppTokenAccountType|[vppTokenAccountType](../resources/intune-shared-vpptokenaccounttype.md)|特定の Apple ボリューム購入プログラムのトークンが関連付けられている、ボリューム購入プログラムの種類。 可能な値は、`business`、`education` です。 可能な値は、`business`、`education` です。|
|appleId|String|特定の Apple ボリューム購入プログラムのトークンに関連付けられている Apple ID。|
|expirationDateTime|DateTimeOffset|Apple ボリューム購入プログラムのトークンの有効期限。|
|lastSyncDateTime|DateTimeOffset|Apple volume purchase program のトークンを使用して、Apple volume purchase program サービスでアプリケーションの同期が最後に実行された時刻。|
|token|String|Apple ボリューム購入プログラムからダウンロードした Apple ボリューム購入プログラムのトークン文字列。|
|lastModifiedDateTime|DateTimeOffset|Apple ボリューム購入プログラムのトークンに関連付けられている最終変更日時。|
|state|[vppTokenState](../resources/intune-onboarding-vpptokenstate.md)|Apple ボリューム購入プログラムのトークンの現在の状態。 可能な値は、`unknown`、`valid`、`expired`、`invalid`、`assignedToExternalMDM` です。 可能な値は、`unknown`、`valid`、`expired`、`invalid`、`assignedToExternalMDM` です。|
|tokenActionResults|[Vpptokenactionresult](../resources/intune-onboarding-vpptokenactionresult.md)コレクション|Apple Volume Purchase Program トークンで実行されたアクションのステータスのコレクション。|
|lastSyncStatus|[vppTokenSyncStatus](../resources/intune-onboarding-vpptokensyncstatus.md)|Apple ボリューム購入プログラム トークンを使用して行われた最後のアプリケーションの同期の現在の同期状態。 可能な値は、`none`、`inProgress`、`completed`、`failed` です。 可能な値は、`none`、`inProgress`、`completed`、`failed` です。|
|automaticallyUpdateApps|Boolean|VPP トークンのアプリを自動で更新するかどうか。|
|countryOrRegion|文字列|VPP トークンのアプリを自動で更新するかどうか。|
|dataSharingConsentGranted|Boolean|Apple Volume Purchase Program でのデータ共有に対して付与される同意。|
|displayName|String|管理者が指定したトークンのフレンドリ名。|
|Msrtcsip-locationname|String|Apple VPP から返されるトークンの場所。|
|claimTokenManagementFromExternalMdm|Boolean|管理者の同意を得て、外部 MDM からのトークン管理を許可します。|
|roleScopeTagIds|文字列コレクション|このエンティティに割り当てられているロールスコープタグ Id。|



## <a name="response"></a>応答
成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [VPPトークン](../resources/intune-onboarding-vpptoken.md) オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/vppTokens/{vppTokenId}
Content-type: application/json
Content-length: 1002

{
  "@odata.type": "#microsoft.graph.vppToken",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "state": "valid",
  "tokenActionResults": [
    {
      "@odata.type": "microsoft.graph.vppTokenActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value",
  "dataSharingConsentGranted": true,
  "displayName": "Display Name value",
  "locationName": "Location Name value",
  "claimTokenManagementFromExternalMdm": true,
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ]
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1115

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
  "tokenActionResults": [
    {
      "@odata.type": "microsoft.graph.vppTokenActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value",
  "dataSharingConsentGranted": true,
  "displayName": "Display Name value",
  "locationName": "Location Name value",
  "claimTokenManagementFromExternalMdm": true,
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ]
}
```





