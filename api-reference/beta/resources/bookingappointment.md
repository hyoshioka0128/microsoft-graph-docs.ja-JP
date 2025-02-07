---
title: bookingappointment リソースの種類
description: " > **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでは、これらの API の使用はサポートされていません。"
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 8b1d481d43374d8611f221fb5c3047cdc9cd9148
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33328232"
---
# <a name="bookingappointment-resource-type"></a>bookingappointment リソースの種類

 [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]
 
Microsoft の予約ビジネスによって提供される、一連のスタッフメンバーによって実行される、 [bookingservice](bookingservice.md)の顧客の予定を表します。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[予定を一覧表示する](../api/bookingbusiness-list-appointments.md) |  [bookingappointment](bookingappointment.md)コレクション | 指定した[bookingappointment](../resources/bookingbusiness.md)の**bookingappointment**オブジェクトのリストを取得します。 |
|[bookingappointment の作成](../api/bookingbusiness-post-appointments.md) |  [bookingAppointment](bookingappointment.md) | 指定した[bookingappointment](../resources/bookingbusiness.md)の新しい**ブック**を作成します。 |
|[bookingappointment を取得する](../api/bookingappointment-get.md) | [bookingAppointment](bookingappointment.md) |**bookingappointment**オブジェクトのプロパティと関係を読み取ります。|
|[Update](../api/bookingappointment-update.md) | [bookingAppointment](bookingappointment.md)    |**bookingappointment**オブジェクトを更新します。 |
|[Delete](../api/bookingappointment-delete.md) | なし |**bookingappointment**オブジェクトを削除します。 |
|[Cancel](../api/bookingappointment-cancel.md)|なし| **bookingappointment**オブジェクトを取り消します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|customerEmailAddress|String|予定を予約している[bookingcustomer](bookingcustomer.md)の SMTP アドレス。|
|id|String|この予定の[bookingcustomer](bookingcustomer.md)の ID。 予定の作成時に ID が指定されていない場合は、新しい**bookingcustomer**オブジェクトが作成されます。 設定すると、 **customerId**を不変にすることを考慮する必要があります。|
|顧客の所在地|[location](location.md)|予定を予約している[bookingcustomer](bookingcustomer.md)の場所情報を表します。|
|おける|String|顧客の名前を指定します。|
|顧客メモ|String|この予定に関連付けられている顧客からのメモ。 ID でこの**bookingappointment**を読み取る場合にのみ、値を取得できます。 <br> このプロパティは、最初に新しい顧客を使用して予定を作成するときにのみ設定できます。 その時点で、その値は**customerId**で表される顧客から計算されます。|
|顧客電話|String|お客様の電話番号。|
|duration|期間|「文字形式」で示されて[](https://www.iso.org/iso-8601-date-and-time-format.html)いる予定の長さ。 |
|end|[dateTimeTimeZone](datetimetimezone.md)|予定が終了する日付、時刻、タイムゾーン。|
|id|String| **bookingappointment**の ID。 読み取り専用です。|
|invoiceAmount|2 行分|請求書の請求金額。|
|invoiceDate|[dateTimeTimeZone](datetimetimezone.md)|この予定の請求書の日付、時刻、タイムゾーン。|
|invoiceId|String|請求書の ID。|
|invoiceStatus|string| 請求書の状態。 使用可能な値: `draft`、`reviewing`、`open`、`canceled`、`paid`、`corrective`。|
|invoiceUrl|String|Microsoft 予約の請求書の URL。|
|optOutOfCustomerEmail|Boolean|True は、この予定の[bookingcustomer](bookingcustomer.md)が、この予定の確認を受信したくないことを示します。|
|postbuffer|期間|予定が終了した後に、クリーンアップのために確保する時間の長さを例として示します。 この値は、" [](https://www.iso.org/iso-8601-date-and-time-format.html) /" という形式で表されます。 |
|prebuffer|期間|準備のために予定が開始されるまでの時間を例として示します。 この値は、" [](https://www.iso.org/iso-8601-date-and-time-format.html) /" という形式で表されます。|
|代金|2 行分|指定した[bookingservice](bookingservice.md)の予定に対する正規の価格。|
|priceType|string| サービスの価格構造を柔軟に提供するための設定。 可能な値は、`undefined`、`fixedPrice`、`startingAt`、`hourly`、`free`、`priceVaries`、`callUs`、`notSet` です。|
|isp|[bookingreminder](bookingreminder.md)コレクション|この予定に対して送信された顧客のアラームのコレクションです。 このプロパティの値は、この**bookingappointment**を ID で読み取る場合にのみ使用できます。|
|selfServiceAppointmentId|String|顧客に代わってスタッフメンバーではなく、顧客が [スケジュール] ページで直接作成された予定の場合は、予定の追加の追跡 ID。|
|serviceId|String|この予定に関連付けられている[bookingservice](bookingservice.md)の ID です。|
|serviceLocation|[location](location.md)|サービスが配信される場所。|
|serviceName|String|この予定に関連付けられている**bookingservice**の名前です。<br>新しい予定を作成するときは、このプロパティは省略可能です。 指定しない場合、 **serviceId**プロパティによって、予定に関連付けられているサービスから計算されます。|
|serviceNotes|String|[bookingStaffMember](bookingstaffmember.md)からのメモ。 このプロパティの値は、この**bookingappointment**を ID で読み取る場合にのみ使用できます。|
|staffMemberIds|String collection|この予定でスケジュールされている各[bookingStaffMember](bookingstaffmember.md)の ID。|
|start|[dateTimeTimeZone](datetimetimezone.md)|予定が開始する日付、時刻、タイムゾーン。|

## <a name="relationships"></a>リレーションシップ
なし


## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingAppointment"
}-->

```json
{
  "customerEmailAddress": "String",
  "customerId": "String",
  "customerLocation": {"@odata.type": "microsoft.graph.location"},
  "customerName": "String",
  "customerNotes": "String",
  "customerPhone": "String",
  "duration": "String (timestamp)",
  "end": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "id": "String (identifier)",
  "invoiceAmount": 1024,
  "invoiceDate": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "invoiceId": "String",
  "invoiceStatus": "string",
  "invoiceUrl": "String",
  "optOutOfCustomerEmail": true,
  "postBuffer": "String (timestamp)",
  "preBuffer": "String (timestamp)",
  "price": 1024,
  "priceType": "string",
  "reminders": [{"@odata.type": "microsoft.graph.bookingReminder"}],
  "selfServiceAppointmentId": "String",
  "serviceId": "String",
  "serviceLocation": {"@odata.type": "microsoft.graph.location"},
  "serviceName": "String",
  "serviceNotes": "String",
  "staffMemberIds": ["String"],
  "start": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "bookingAppointment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
