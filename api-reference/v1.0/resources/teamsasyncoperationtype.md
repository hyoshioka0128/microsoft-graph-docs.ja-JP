---
title: teamsAsyncOperationType 列挙型
description: teamsAsyncOperation の種類。 より多くの非同期操作がサポートされているので、メンバーが追加されます。
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 3866c41b74fc6748479099d43b268afa115dde67
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32462236"
---
# <a name="teamsasyncoperationtype-enum-type"></a>teamsAsyncOperationType 列挙型

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[teamsAsyncOperation](teamsasyncoperation.md)の種類。 より多くの非同期操作がサポートされているので、メンバーが追加されます。

## <a name="members"></a>メンバー

| メンバー | 値| 説明 |
|:---------------|:--------|:----------|
|無効です|.0|無効な値です。|
|cloneTeam|1-d|チームを複製する操作。|
|アーカイブチーム|pbm-2|チームをアーカイブする操作。|
|アーカイブなしのチーム|1/3|アーカイブされたチームを復元する操作。|
|teamsasyncoperationtype|1/3|最初からチームを作成する操作。|

<!--
{
  "type": "#page.annotation",
  "suppressions": [
    "Error: /api-reference/beta/resources/teamsasyncoperationtype.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
