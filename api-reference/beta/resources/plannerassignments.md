---
title: プランの割り当てリソースの種類
description: '[ **plan** ] [割り当て] リソースは、"プラン" タスクリソースの割り当てを表します。 この型はオープン型です。 この型の各プロパティの名前 '
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 2f26bab4eb69a79f4bd18f80128e4445217a1ae7
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33344572"
---
# <a name="plannerassignments-resource-type"></a>プランの割り当てリソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[ **plan** ] [割り当て] リソースは、"[プラン" タスク](plannertask.md)リソースの割り当てを表します。 この型はオープン型です。 この型の各プロパティ名は、タスクが割り当てられているユーザーオブジェクトの ID です。 ユーザーは、ID でという名前の新しいプロパティを作成してタスクに割り当てることができます。このオブジェクトには、値として orderhint プロパティが設定された[プランの assignment](plannerassignment.md)オブジェクトがあります。 parenttab の ID を null に設定することによって、タスクの割り当てを解除することができます。


## <a name="properties"></a>プロパティ
オープン型のプロパティは、クライアントで定義できます。 ただし、この場合、クライアントは、割り当てられたユーザーの id をプロパティ名として提供する必要があります。 タスク実施者を作成または変更するには、このプロパティを**plan**オブジェクトに設定する必要があります。削除するには null に設定する必要があります。

例:

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignments"
}-->

```json
{
  "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47": null,
  "4e98f8f1-bb03-4015-b8e0-19bb370949d8": { 
      "@odata.type": "microsoft.graph.plannerAssignment",
      "orderHint": "String"
    }
}
```
この例では、id ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 を持つユーザーをタスクのタスク実施者リストから削除し、ユーザー id 4e98f8f1-bb03-4015-b8e0-19bb370949d8 を使用して担当者の順序を変更します。 タスクが ID 4e98f8f1-bb03-4015-b8e0-19bb370949d8 のユーザーにまだ割り当てられていない場合は、この値を使用して割り当てを更新すると、このユーザーにタスクが割り当てられます。

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerAssignments resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
