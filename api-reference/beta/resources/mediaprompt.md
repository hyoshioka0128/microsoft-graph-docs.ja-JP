---
title: mediaprompt リソースの種類
description: mediaprompt の種類。
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: aa08436d46777b4e82712e3288ec17047c33a1ff
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342633"
---
# <a name="mediaprompt-resource-type"></a>mediaprompt リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

mediaprompt の種類。

## <a name="properties"></a>プロパティ

| プロパティ    | 型                      | 説明                                                                     |
| :---------- | :------------------------ | :------------------------------------------------------------------------------ |
| for        | Int32                     | ループカウント。 0は無限にループすることを示します。 既定値は `1` です。 |
| mediaInfo   | [mediaInfo](mediainfo.md) | メディア情報                                                           |

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->

```json
{
  "loop": 1024,
  "mediaInfo": { "@odata.type": "#microsoft.graph.mediaInfo" }
}
```

## <a name="example"></a>例

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->
```json
{
  "mediaInfo": {
    "uri": "https://cdn.contoso.com/beep.wav",
    "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
  },
  "loop": 5
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "mediaPrompt resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
