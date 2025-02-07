---
title: teamDiscoverySettings リソースの種類
description: 他のユーザーがチームの探索可能性を構成するための設定。
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: 56284b678dec74e00724eeb429958aa54444208d
ms.sourcegitcommit: b742da101a3a232356bf748c42da3ba08a7539d3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2019
ms.locfileid: "34818705"
---
# <a name="teamdiscoverysettings-resource-type"></a>teamDiscoverySettings リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

他のユーザーが[チーム](team.md)の検出を構成できるようにするための設定を提供します。 プライベートチームの探索設定のみを変更できます。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|showInTeamsSearchAndSuggestions|Boolean|True に設定されている場合、チームは、Teams クライアントからの検索と提案によって参照できます。|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamDiscoverySettings"
}-->

```json
{
  "showInTeamsSearchAndSuggestions": true
}
```

<!-- uuid: f1d42106-0b3d-4930-9f19-d76f4e03b36b
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's discoverySettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/teamdiscoverysettings.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}-->
