---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/11/2017
title: ColumnDefinition
localization_priority: Normal
ms.openlocfilehash: 679f0139f7ad0e94eab1970cc113268a56722663
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32584853"
---
# <a name="columndefinition-resource"></a>ColumnDefinition リソース

## <a name="json-representation"></a>JSON 表記

以下は、ColumnDefinition リソースの JSON 表記です。

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.columnDefinition"
}-->

```json
{
  "columnGroup": "string",
  "description": "description",
  "displayName": "friendly name",
  "enforceUniqueValues": "true",
  "hidden": false,
  "id": "string",
  "indexed": true,
  "name": "staticNameForApi",
  "readOnly": false,
  "required": false,
  "boolean": { "@odata.type": "microsoft.graph.booleanColumn" },
  "calculated": { "@odata.type": "microsoft.graph.calculatedColumn" },
  "choice": { "@odata.type": "microsoft.graph.choiceColumn" },
  "currency": { "@odata.type": "microsoft.graph.currencyColumn" },
  "dateTime": { "@odata.type": "microsoft.graph.dateTimeColumn" },
  "defaultValue": { "@odata.type": "microsoft.graph.defaultColumnValue" },
  "lookup": { "@odata.type": "microsoft.graph.lookupColumn" },
  "number": { "@odata.type": "microsoft.graph.numberColumn" },
  "personOrGroup": { "@odata.type": "microsoft.graph.personOrGroupColumn" },
  "text": { "@odata.type": "microsoft.graph.textColumn" }
}
```

## <a name="properties"></a>プロパティ

**columnDefinition** リソースには以下のプロパティがあります。

| プロパティ名           | 種類    | 説明
|:------------------------|:--------|:-----------------------------------------
| **columnGroup**         | string  | サイト列の場合、この列が属するグループの名前。 関連する列を整理するのに役立ちます。
| **説明**         | string  | 列に関するユーザー向けの説明。
| **displayName**         | string  | 列を示すユーザー向けの名前。
| **enforceUniqueValues** | ブール値 | True の場合、この列で 2 つのリスト アイテムの値を同じにすることはできません。
| **hidden**              | ブール値 | この列がユーザー インターフェイスに表示されるかどうかを指定します。
| **id**                  | string  | 列の一意識別子。
| **indexed**             | ブール値 | 列の値を、並べ替えと検索に使用できるかどうかを指定します。
| **name**                | string  | [listItem][] の [fields][] に表示される、列を示す API 向けの名前。 ユーザー向けの名前については **displayName** をご覧ください。
| **readOnly**            | bool    | 列の値を変更できるかどうかを指定します。
| **required**            | boolean | 列の値が省略不可であるかどうかを指定します。

列には、さまざまな種類のデータを保持できます。
次のプロパティは、列に保持されるデータの種類と、そのデータに関する追加の設定を示します。
これらのプロパティは相互に排他的で、各列でいずれか 1 つだけを指定できます。

| プロパティ名     | 種類                    | 説明
|:------------------|:------------------------|:-------------------------------
| **boolean**       | [booleanColumn][]       | この列にはブール値が格納されます。
| **calculated**    | [calculatedColumn][]    | この列のデータは、他の列に基づいて計算されます。
| **choice**        | [choiceColumn][]        | この列には、選択肢リストからのデータが格納されます。
| **currency**      | [currencyColumn][]      | この列には通貨値が格納されます。
| **dateTime**      | [dateTimeColumn][]      | この列には日時の値が格納されます。
| **defaultValue**  | [defaultColumnValue][]  | この列の既定値です。
| **lookup**        | [lookupColumn][]        | この列のデータは、サイト内の別のソースから検索されます。
| **number**        | [numberColumn][]        | この列には数値が格納されます。
| **personOrGroup** | [personOrGroupColumn][] | この列にはユーザーまたはグループの値が格納されます。
| **text**          | [textColumn][]          | この列にはテキスト値が格納されます。

注: これらのプロパティは SharePoint の [SPFieldType][] 列挙体に対応しています。
最も一般的なフィールドの種類は上記のとおりですが、この API はまだ一部不足しています。
そのような場合、どの列タイプ ファセットも入力されず、基本的なプロパティだけが列に含まれます。

## <a name="remarks"></a>備考

`hidden` 列の ColumnDefinitions とフィールドの値は、既定では表示されません。
**columnDefinitions** を一覧表示するときにこれらが表示されるようにするには、`$select` ステートメントに `hidden` を含めます。
[listItems][listItem] の**フィールド**値を表示するときにこれらが表示されるようにするには、`$select` ステートメントに目的の列の名前を含めます。

[booleanColumn]: booleancolumn.md
[calculatedColumn]: calculatedcolumn.md
[choiceColumn]: choicecolumn.md
[currencyColumn]: currencycolumn.md
[dateTimeColumn]: datetimecolumn.md
[defaultColumnValue]: defaultcolumnvalue.md
[lookupColumn]: lookupcolumn.md
[numberColumn]: numbercolumn.md
[personOrGroupColumn]: personorgroupcolumn.md
[textColumn]: textcolumn.md
[fieldValueSet]: fieldvalueset.md
[fields]: fieldvalueset.md
[listItem]: listitem.md

[SPFieldType]: https://msdn.microsoft.com/library/microsoft.sharepoint.spfieldtype.aspx

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnDefinition"
} -->
