---
title: SharePoint アクティビティ レポート
description: SharePoint の使用を許可されているすべてのユーザーのアクティビティを取得するには、ファイルとの相互作用を参照してください。 共有されたファイル数に基づいて、進行中のコラボレーションのレベルを確認することもできます。
localization_priority: Normal
ms.prod: reports
author: pranoychaudhuri
ms.openlocfilehash: cfe8c698533b46d4edbbb724dc5fb993cc85cfdb
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33343169"
---
# <a name="sharepoint-activity-reports"></a>SharePoint アクティビティ レポート

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

SharePoint の使用を許可されているすべてのユーザーのアクティビティを取得するには、ファイルとの相互作用を参照してください。 共有されたファイル数に基づいて、進行中のコラボレーションのレベルを確認することもできます。

> **注:** 別のレポートのビューとレポート名についての詳細は、「[Office 365 レポート: SharePoint アクティビティ](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f)」を参照してください。

## <a name="reports"></a>レポート

| 関数                                 | CSV 戻り値の型 | JSON 戻り値の種類                         | 説明                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [ユーザーの詳細を取得する](../api/reportroot-getsharepointactivityuserdetail.md) | ストリーム          | [sharepointactivityuserdetail](../resources/sharepointactivityuserdetail.md) | ユーザー別の SharePoint アクティビティに関する詳細を取得します。 |
| [ファイルの数を取得する](../api/reportroot-getsharepointactivityfilecounts.md) | Stream          | [siteactivitysummary](../resources/siteactivitysummary.md) | SharePoint サイトに保存されているファイルを操作した、それぞれ別個のライセンス ユーザーの数を取得します。 |
| [ユーザーの数を取得する](../api/reportroot-getsharepointactivityusercounts.md) | Stream          | [sharepointactivityusercounts](../resources/sharepointactivityusercounts.md) | アクティブ ユーザーの数の傾向を取得します。 ユーザーが一定期間中にファイル アクティビティ (保存、同期、変更、共有) を実行するか、またはページにアクセスすると、そのユーザーはアクティブとみなされます。 |
| [ページを取得する](../api/reportroot-getsharepointactivitypages.md) | Stream          | [sharePointActivityPages](../resources/sharepointactivitypages.md) | ユーザーがアクセスしたそれぞれ別個のページ数を取得します。 |
