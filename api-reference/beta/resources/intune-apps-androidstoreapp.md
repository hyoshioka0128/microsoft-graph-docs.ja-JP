---
title: androidStoreApp リソース タイプ
description: Android ストア アプリのプロパティと継承されるプロパティを含みます。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 64d90c8c3bb2c891ec57c863c7238f30f4e2358e
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34991270"
---
# <a name="androidstoreapp-resource-type"></a>androidStoreApp リソース タイプ

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android ストア アプリのプロパティと継承されるプロパティを含みます。


[mobileApp](../resources/intune-apps-mobileapp.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List androidStoreApps](../api/intune-apps-androidstoreapp-list.md)|[androidStoreApp](../resources/intune-apps-androidstoreapp.md) コレクション|[androidStoreApp](../resources/intune-apps-androidstoreapp.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get androidStoreApp](../api/intune-apps-androidstoreapp-get.md)|[androidStoreApp](../resources/intune-apps-androidstoreapp.md)|[androidStoreApp](../resources/intune-apps-androidstoreapp.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create androidStoreApp](../api/intune-apps-androidstoreapp-create.md)|[androidStoreApp](../resources/intune-apps-androidstoreapp.md)|新しい [androidStoreApp](../resources/intune-apps-androidstoreapp.md) オブジェクトを作成します。|
|[Delete androidStoreApp](../api/intune-apps-androidstoreapp-delete.md)|なし|[androidStoreApp](../resources/intune-apps-androidstoreapp.md) を削除します。|
|[Update androidStoreApp](../api/intune-apps-androidstoreapp-update.md)|[androidStoreApp](../resources/intune-apps-androidstoreapp.md)|[androidStoreApp](../resources/intune-apps-androidstoreapp.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|エンティティのキー。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|displayName|文字列|管理者が提供またはインポートしたアプリのタイトル。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|description|String|アプリの説明。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|publisher|String|アプリの発行元。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|largeIcon|[mimeContent](../resources/intune-shared-mimecontent.md)|アプリの詳細に表示され、アイコンのアップロードに使用される大きいアイコン。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|createdDateTime|DateTimeOffset|アプリが作成された日時。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|アプリが最後に変更された日時。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|isFeatured|Boolean|アプリが管理者のおすすめとしてマークされたかどうかを示す値。[mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|privacyInformationUrl|String|プライバシーに関する声明の URL。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|informationUrl|String|詳細情報の URL。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|owner|String|アプリの所有者。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|developer|String|アプリの開発者。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|notes|String|アプリ用のメモ。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|uploadState|Int32|アップロード状態。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|publishingState|[mobileAppPublishingState](../resources/intune-apps-mobileapppublishingstate.md)|アプリの発行の状態。 アプリが発行されていない限り、アプリを割り当てることができません。 [MobileApp](../resources/intune-apps-mobileapp.md)から継承されます。 可能な値は、`notPublished`、`processing`、`published` です。|
|isAssigned|Boolean|アプリが少なくとも1つのグループに割り当てられているかどうかを示す値。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|roleScopeTagIds|文字列コレクション|このモバイルアプリの範囲タグ id のリスト。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|dependentAppCount|Int32|子アプリが持つ依存関係の合計数。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|packageId|文字列型 (String)|パッケージの識別子。|
|appIdentifier|String|ID 名。|
|appStoreUrl|String|Android アプリ ストアの URL。|
|minimumSupportedOperatingSystem|[androidMinimumOperatingSystem](../resources/intune-apps-androidminimumoperatingsystem.md)|該当するオペレーティング システムの最小の値です。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|categories|[mobileAppCategory](../resources/intune-apps-mobileappcategory.md) コレクション|このアプリのカテゴリのリスト。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|assignments|[mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) コレクション|このモバイル アプリのグループ割り当てのリスト。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|installSummary|[mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md)|モバイル アプリ インストール概要です。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|deviceStatuses|[mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)コレクション|このモバイルアプリのインストール状態のリスト。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|userStatuses|[Userappinstallstatus](../resources/intune-apps-userappinstallstatus.md)コレクション|このモバイルアプリのインストール状態のリスト。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|
|関連性|[mobileAppRelationship](../resources/intune-apps-mobileapprelationship.md)コレクション|このモバイルアプリのリレーションシップのリスト。 [mobileApp](../resources/intune-apps-mobileapp.md) から継承します|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidStoreApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidStoreApp",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "uploadState": 1024,
  "publishingState": "String",
  "isAssigned": true,
  "roleScopeTagIds": [
    "String"
  ],
  "dependentAppCount": 1024,
  "packageId": "String",
  "appIdentifier": "String",
  "appStoreUrl": "String",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true,
    "v6_0": true,
    "v7_0": true,
    "v7_1": true,
    "v8_0": true,
    "v8_1": true,
    "v9_0": true
  }
}
```





