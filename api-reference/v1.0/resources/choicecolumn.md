---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/11/2017
title: ChoiceColumn
localization_priority: Normal
ms.openlocfilehash: 1dddbd4cfa4f26ecc0fd79a430c9d7f725bebbf9
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32584997"
---
# <a name="choicecolumn-resource-type"></a>ChoiceColumn リソースの種類

[columnDefinition ](columndefinition.md)リソースの** choiceColumn **は、選択肢のリストから列の値を選択できることを示します。

## <a name="json-representation"></a>JSON 表記

以下は、**choiceColumn** リソースの JSON 表記です。
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.choiceColumn" } -->

```json
{
  "allowTextEntry": true,
  "choices": ["red", "blue", "green"],
  "displayAs": "checkBoxes | dropDownMenu | radioButtons"
}
```

## <a name="properties"></a>プロパティ

| プロパティ名      | 種類               | 説明
|:-------------------|:-------------------|:----------------------------------------------
| **allowTextEntry** | boolean            | true の場合、設定された選択肢にないカスタム値を使用できます。
| **choices**        | collection(string) | この列に使用可能な値のリスト。
| **displayAs**      | string             | UX での選択肢の表示方法。 `checkBoxes`、`dropDownMenu`、`radioButtons` のいずれかでなければなりません。


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/choicecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(checkBoxes,dropDownMenu,radioButtons) are in resource, but () are in table"
  ],
  "tocPath": "Resources/ChoiceColumn"
} -->
