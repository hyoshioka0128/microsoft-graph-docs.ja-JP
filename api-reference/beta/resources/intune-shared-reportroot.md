---
title: reportRoot リソースの種類
description: コンテキストに応じて、デバイスのインスタンスまたはトラブルシューティングレポートを表すリソース。
localization_priority: Normal
author: rolyon
ms.prod: intune
ms.openlocfilehash: c975abfa3cb580d107967c7adaf66627bad2ad2e
ms.sourcegitcommit: 94aaf594c881c02f353c6a417460cdf783a0bfe0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2019
ms.locfileid: "33938731"
---
# <a name="reportroot-resource-type"></a>reportRoot リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

コンテキストに応じて、デバイスのインスタンスまたはトラブルシューティングレポートを表すリソース。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[ReportRoot の取得](../api/intune-shared-reportroot-get.md)|[reportRoot](../resources/intune-shared-reportroot.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[reportRoot の更新](../api/intune-shared-reportroot-update.md)|[reportRoot](../resources/intune-shared-reportroot.md) オブジェクトのプロパティを更新します。|
|**デバイス構成**|
|[deviceConfigurationUserActivity function](../api/intune-shared-reportroot-deviceconfigurationuseractivity.md)|デバイス構成のユーザー アクティビティ レポートのメタデータ|
|[deviceConfigurationDeviceActivity function](../api/intune-shared-reportroot-deviceconfigurationdeviceactivity.md)|デバイス構成のデバイス アクティビティ レポートのメタデータ|
|**トラブルシューティング**|
|[managedDeviceEnrollmentAbandonmentDetails 関数](../api/intune-shared-reportroot-manageddeviceenrollmentabandonmentdetails.md)|[レポート](../resources/intune-shared-report.md)|登録 abandonment 詳細レポートのメタデータ|
|[managedDeviceEnrollmentAbandonmentSummary 関数](../api/intune-shared-reportroot-manageddeviceenrollmentabandonmentsummary.md)|[レポート](../resources/intune-shared-report.md)|登録 abandonment の概要レポートのメタデータ|
|[managedDeviceEnrollmentFailureDetails 関数](../api/intune-shared-reportroot-manageddeviceenrollmentfailuredetails.md)|まだ文書化されていません|
|[managedDeviceEnrollmentFailureTrends 関数](../api/intune-shared-reportroot-manageddeviceenrollmentfailuretrends.md)|登録失敗傾向レポートのメタデータ|
|[managedDeviceEnrollmentTopFailures 関数](../api/intune-shared-reportroot-manageddeviceenrollmenttopfailures.md)|まだ文書化されていません|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|このエンティティの一意識別子です。|

## <a name="relationships"></a>関係
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.reportRoot"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "String (identifier)"
}
```



