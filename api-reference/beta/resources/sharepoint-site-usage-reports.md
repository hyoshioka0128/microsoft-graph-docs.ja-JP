---
title: SharePoint サイト使用状況レポート
description: sharepoint サイトにユーザーが格納しているファイルの総数、使用されているファイルの数、およびこれらのすべてのサイトで使用されているストレージの数に関して、sharepoint から取得した値の概要を把握することができます。 その後、[SharePoint サイトの利用状況] レポートを詳細に確認して、すべてのサイトの傾向およびサイトごとのレベル詳細を把握できます。
localization_priority: Normal
ms.prod: reports
author: pranoychaudhuri
ms.openlocfilehash: 856680732b7dce1b6e0b83105c64d86b72897967
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33343159"
---
# <a name="sharepoint-site-usage-reports"></a>SharePoint サイト使用状況レポート

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

sharepoint サイトにユーザーが格納しているファイルの総数、使用されているファイルの数、およびこれらのすべてのサイトで使用されているストレージの数に関して、sharepoint から取得した値の概要を把握することができます。 その後、[SharePoint サイトの利用状況] レポートを詳細に確認して、すべてのサイトの傾向およびサイトごとのレベル詳細を把握できます。

> **注:** 別のレポートのビューとレポート名についての詳細は、「[Office 365 レポート: SharePoint サイトの使用状況](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)」を参照してください。

## <a name="reports"></a>レポート

| 関数                                 | CSV 戻り値の型 | JSON 戻り値の種類                         | 説明                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [サイトの詳細を取得する](../api/reportroot-getsharepointsiteusagedetail.md) | Stream          | [sharepointsiteの詳細情報](../resources/sharepointsiteusagedetail.md) | SharePoint サイトの使用状況に関する詳細を取得します。 |
| [ファイルの数を取得する](../api/reportroot-getsharepointsiteusagefilecounts.md) | Stream          | [sharePointSiteUsageFileCounts](../resources/sharepointsiteusagefilecounts.md) | すべてのサイトのファイルの合計数と、アクティブ ファイルの数を取得します。 ファイル (ユーザーまたはシステム) は、一定期間中に保存、同期、変更、共有されるとアクティブとみなされます。 |
| [サイトの数を取得する](../api/reportroot-getsharepointsiteusagesitecounts.md) | Stream          | [sharepointsiteusagesitecounts](../resources/sharepointsiteusagesitecounts.md) | すべてのサイトのファイルの合計数と、アクティブ ファイルの数を取得します。 ファイル (ユーザーまたはシステム) は、一定期間中に保存、同期、変更、共有されるとアクティブとみなされます。 |
| [ストレージを取得する](../api/reportroot-getsharepointsiteusagestorage.md) | Stream          | [サイトの保存場所](../resources/siteusagestorage.md) | レポート期間中に割り当てられ、消費したストレージの傾向を取得します。 |
| [ページを取得する](../api/reportroot-getsharepointsiteusagepages.md) | Stream          | [sharepointsiteのページ](../resources/sharepointsiteusagepages.md) | すべてのサイトで表示されたページ数を取得します。 |
