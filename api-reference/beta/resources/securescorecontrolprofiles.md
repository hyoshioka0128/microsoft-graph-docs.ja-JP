---
title: secureScoreControlProfile リソースの種類
description: テナントのセキュリティスコア (コントロールデータごと) を表します。 既定では、テナントのすべてのコントロールを返し、個々のコントロールを明示的に取得することができます。
localization_priority: Normal
ms.openlocfilehash: 41a74af0de47bbe77b8ea04cbea011a6f085d1bb
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33343412"
---
# <a name="securescorecontrolprofile-resource-type"></a>secureScoreControlProfile リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

テナントのセキュリティスコア (コントロールデータごと) を表します。 既定では、テナントのすべてのコントロールを返し、個々のコントロールを明示的に取得することができます。


## <a name="methods"></a>メソッド

| メソッド   | 戻り値の型|説明|
|:---------------|:--------|:----------|
|[secureScoreControlProfiles のリスト](../api/securescorecontrolprofiles-list.md) | [secureScoreControlProfile](securescorecontrolprofiles.md)コレクション |secureScoreControlProfile オブジェクトのコレクションを取得します。|


## <a name="properties"></a>プロパティ

|名前 |型 |説明 |
|:--|:--|:--|
|   azureTenantId   |   String  |   テナント ID の GUID 文字列。  |
|   controlName |   String  |   コントロールの名前を指定します。 |
|   title   |   String  |   コントロールのタイトルを指定します。   |
| complianceInformation | [complianceInformation](complianceinformation.md)コレクション | セキュリティで保護されたスコアコントロールに関連付けられているコンプライアンス情報のコレクション |
|   controlcategory |   String  |   コントロールアクションカテゴリ (アカウント、データ、デバイス、アプリ、インフラストラクチャ)。  |
|   actionType  |   String  |   アクションの種類 (Config、Review、Behavior) を制御します。 |
|   service |   String  |   コントロールを所有するサービス (Exchange、Sharepoint、Azure AD)。 |
|   maxscore |  String  |   指定された日付における現在の取得最高スコア。   |
|   層 |  String  |   Control 層 (コア、多層防御、詳細)    |
|   userimpact |    String  | 制御を実装するユーザーへの影響 (低、中、高)。    |
|   implementationCost |    String  |   implemmentating コントロールのリソースコスト (低、中、高)。 |
|   rank |  Int32   |   Microsoft のスタックランキング。   |
|   主 |   String コレクション   |   統制によって軽減される脅威のリスト (accountbreach、datadeletion、dataexのフィルター、dataSpillage、elevationOfPrivilege、maliciousInsider、passwordcracking、phishingOrWhaling、スプーフィング)。 |
|   予定 |    Boolean |   コントロールが減価償却されているかどうかを示すフラグです。   |
|   修復 |   String  |   修復に役立つコントロールの説明。 |
|   remediationImpact | String  |   修復のユーザーへの影響についての説明。 |
|   actionUrl | String  |   コントロールを actioned できる場所の URL。 |
|   controlstateupdates | [secureScoreControlStateUpdate](securescorecontrolstateupdate.md)コレクション |    テナントがコントロールをマークした場所を示すフラグ (ignore、thirdParty、レビュー済み) ([更新プログラム](../api/securescorecontrolprofiles-update.md)をサポート)。 |
|   vendorInformation | [securityVendorInformation](securityvendorinformation.md) |

## <a name="relationships"></a>リレーションシップ

なし。

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.secureScoreControlProfile"
}-->

```json
{
  "title": "String",
  "azureTenantId": "String (identifier)",
  "maxScore": 1024.13,
  "actionType": "String",
  "service": "String",
  "tier": "String",
  "userImpact": "string",
  "implementationCost ": "String",
  "rank ": 100,
  "threats": ["string"],
  "deprecated ": false,
  "remediation": "String",
  "remediationImpact ": "String",
  "actionUrl": "String",
  "controlStateUpdates": [{"@odata.type": "microsoft.graph.secureScoreControlStateUpdate"}],
  "vendorInformation": {"@odata.type": "microsoft.graph.securityVendorInformation"},
  "complianceInformation": [{"@odata.type": "microsoft.graph.complianceInformation"}],
  "controlCategory": "string",
  "lastModifiedDateTime": "String (timestamp)"
}


```


<!--
{
  "type": "#page.annotation",
  "description": "secureScoreControlProfiles resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
