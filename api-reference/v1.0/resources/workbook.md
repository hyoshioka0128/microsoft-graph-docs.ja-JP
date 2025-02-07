---
title: Workbook リソースタイプ
description: Workbook は、ワークシート、テーブル、範囲などの関連するブック オブジェクトを含む最上位オブジェクトです。
localization_priority: Priority
author: lumine2008
ms.prod: excel
ms.openlocfilehash: b4f0a439db5cc430e558f2d43215cb1c5c0f7779
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32456872"
---
# <a name="workbook-resource-type"></a>Workbook リソースタイプ

Workbook は、ワークシート、テーブル、範囲などの関連するブック オブジェクトを含む最上位オブジェクトです。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbook"
}-->

```json
{
  "names": [{"@odata.type": "microsoft.graph.workbookNamedItem"}],
  "tables": [{"@odata.type": "microsoft.graph.workbookTable"}],
  "worksheets": [{"@odata.type": "microsoft.graph.workbookWorksheet"}]
}
```

## <a name="properties"></a>プロパティ
なし

## <a name="methods"></a>メソッド

| メソッド       | 戻り値の型  |説明|
|:---------------|:--------|:----------|
|[セッションを作成する](../api/workbook-createsession.md) | [workbookSessionInfo](workbooksessioninfo.md) |永続または非永続セッションを開始するために、ブック セッションを作成します。|
|[セッションを閉じる](../api/workbook-closesession.md) | なし |既存のセッションを終了します。|
|[セッションを最新の情報に更新](../api/workbook-refreshsession.md) | なし |既存のセッションを更新します。|


## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|names|[WorkbookNamedItem](nameditem.md) コレクション|ブック スコープの名前付き項目 (名前付き範囲と名前付き定数) のコレクションを表します。読み取り専用。|
|テーブル|[WorkbookTable](table.md) コレクション|ブックに関連付けられているテーブルのコレクションを表します。読み取り専用。|
|worksheets|[WorkbookWorksheet](worksheet.md) コレクション|ブックに関連付けられているワークシートのコレクションを表します。読み取り専用。|

## <a name="functions"></a>関数

[Excel の関数](#functions):構文 `POST /workbook/functions/{function-name}` を使用し、また JSON オブジェクトを使用して本文の関数の引数を提供することでブック関数を呼び出します。関数の結果としての `value` および任意の `error` 文字列が、関数の結果のオブジェクトに返されます。`null` の `error` 値は、関数の実行が成功したことを示します。 

サポートされている関数の完全な一覧は、[こちら](https://support.office.com/ja-JP/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188) です。特定のパラメーター名とデータ型については関数のシグネチャを参照してください。

_重要な注意点: _ 
* 範囲入力パラメーターは、範囲のアドレス文字列ではなく、range オブジェクトを使用して提供されます。  
* Index パラメーターは、API のほとんどで使用されている 0 オリジンとは異なり、1 オリジンのインデックス (添字が 1 から始まる) です。 

例: **vlookup**

Excel スプレッドシートで、`vlookup` 関数は次の引数を取ります。

1. 参照値とも呼ばれる、検索対象の値。
2. 参照値が所在する範囲。 参照値が正しく動作するには、常に VLOOKUP の範囲で参照値が最初の列にある必要があることに留意してください。 たとえば、参照値がセル C2 にある場合、範囲は C 列から始まる必要があります。
3. 戻り値を含む範囲の列番号。 たとえば、B2: D11 を範囲として指定すると、B を最初の列、C を 2 番目の列というようにカウントする必要があります。
4. また、戻り値の近似一致を使用する場合は TRUE を指定し、完全一致を必要とする場合は FALSE を指定することもできます。 何も指定しない場合、既定値は常に TRUE、つまり近似一致になります。

セル内では、`vlookup` 関数は次のようになります。 

=VLOOKUP(<参照値>, <参照値を含む範囲>, <戻り値を含む範囲内の列番号>, <近似一致には TRUE、完全一致には FALSE をオプションで指定>)

([VLOOKUP Excel 関数](https://support.office.com/ja-JP/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1)についてのドキュメントを参照してください。)

次の例では、Excel REST API で `vlookup` 関数を呼び出し、これらのパラメーターを渡す方法を示しています。

要求: 

```http 
POST https://graph.microsoft.com/beta/me/drive/root:/book1.xlsx:/workbook/functions/vlookup
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
    "lookupValue": "Temperature",
    "tableArray": { "Address": "Sheet1!E1:G5" },
    "colIndexNum": 2,
    "rangeLookup": false
}
```

応答:

```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#workbookFunctionResult",
    "@odata.type": "#microsoft.graph.workbookFunctionResult",
    "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/root/workbook/functions/vlookup()",
    "error": null,
    "value": "28.3"
}
```

例: `median`

Excel スプレッドシートでは、`median` 関数は 1 つ以上の入力範囲の配列を取ります。

セル内では、`median` 関数は次の例のようになります。

=MEDIAN(A2:A6)

([MEDIAN Excel 関数](https://support.office.com/ja-JP/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2)についてのドキュメントを参照してください。)

次の例では、Excel REST API で `median` 関数と 1 つ以上の入力範囲を呼び出す方法を示しています。 

要求: 

```http 
POST https://graph.microsoft.com/beta/me/drive/root:/book1.xlsx:/workbook/functions/median
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
"values" :  [
        { "address": "Sheet2!A1:A5" },
        { "address": "Sheet2!B1:B5" },
      ] 
}
```

応答:

```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#workbookFunctionResult",
  "@odata.type": "#microsoft.graph.workbookFunctionResult",
  "@odata.id": "/users('2abcad6a-2fca-4b6e-9577-e358a757d77d')/drive/root/workbook/functions/median()",
  "error": null,
  "value": 30
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Workbook resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
