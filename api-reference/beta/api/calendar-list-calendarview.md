---
title: calendarView を一覧表示する
description: 時間範囲で定義した予定表ビューから、予定、例外、およびイベントの単一インスタンスを取得し、
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: d69b6954faa464444c99a74bfb93cf90dea9eac4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35438910"
---
# <a name="list-calendarview"></a>calendarView を一覧表示する

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

ユーザーまたはグループの既定の予定表 `(../me/calendarview)` またはユーザーが所有する他の予定表から、時間範囲で定義した予定表ビューのイベントの発生、例外、および単一インスタンスを取得します。

## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

* ユーザーの予定表のイベント:Calendars.Read または Calendars.ReadWrite
* グループの予定表のイベント:Group.Read.All または Group.ReadWrite.All

## <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
ユーザーまたはグループの既定の[予定表](../resources/calendar.md)。
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

既定の [calendarGroup](../resources/calendargroup.md) のユーザーの[予定表](../resources/calendar.md)。
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

特定の [calendarGroup](../resources/calendargroup.md) のユーザーの[予定表](../resources/calendar.md)。
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a>クエリ パラメーター

要求 URL に、次の必須のクエリ パラメーターを値で指定します。

| パラメーター    | 型   |説明|
|:---------------|:--------|:----------|
|startDateTime|String|時間範囲の開始日時は、ISO 8601 形式で表されます。例: "2015-11-08T19:00:00.0000000"。|
|endDateTime|String|時間範囲の終了日時は、ISO 8601 形式で表されます。例: "2015-11-08T20:00:00.0000000"。|

また、このメソッドは応答をカスタマイズするための [OData クエリ パラメーター](https://developer.microsoft.com/graph/docs/concepts/query_parameters)もサポートします。
## <a name="request-headers"></a>要求ヘッダー
| 名前       | 型 | 説明 |
|:---------------|:--------|:--------|
| Authorization  | string | ベアラー {トークン}。必須。  |
| 優先: outlook.timezone  | string | これを使用して、応答内の開始および終了時刻のタイム ゾーンを指定します。 指定しない場合、これらの時刻値は UTC で返されます。 省略可能。 |

## <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。

## <a name="response"></a>応答

成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [Event](../resources/event.md) オブジェクトのコレクションを返します。
## <a name="example"></a>例
##### <a name="request"></a>要求
以下は、要求の例です。

# <a name="httptabhttp"></a>[プロトコル](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/beta/me/calendar/calendarView?startDateTime=2017-01-01T19:00:00.0000000&endDateTime=2017-01-07T19:00:00.0000000
```
# <a name="ctabcsharp"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-calendarview-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[Javascript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-calendarview-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[目的-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-calendarview-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 354

{
  "value": [
    {
      "originalStartTimeZone": "originalStartTimeZone-value",
      "originalEndTimeZone": "originalEndTimeZone-value",
      "responseStatus": {
        "response": "response-value",
        "time": "2016-10-19T10:37:00Z"
      },
      "uid": "iCalUId-value",
      "reminderMinutesBeforeStart": 99,
      "isReminderOn": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
