---
title: 'ノートブック: getRecentNotebooks'
description: サインインしたユーザーによってアクセスされた recentNotebook インスタンスの一覧を取得します。
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 0ed8765dd5162d95932be6c4556b986579f9af1b
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33338230"
---
# <a name="notebook-getrecentnotebooks"></a>ノートブック: getRecentNotebooks

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

サインインしたユーザーによってアクセスされた [recentNotebook](../resources/recentnotebook.md) インスタンスの一覧を取得します。

## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | Notes.Create、Notes.Read、Notes.ReadWrite、Notes.Read.All、Notes.ReadWrite.All、|
|委任 (個人用 Microsoft アカウント) | Notes.Create、Notes.Read、Notes.ReadWrite |
|アプリケーション | Notes.Read.All、Notes.ReadWrite.All |

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
GET /users/{id | userPrincipalName}/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
```

ユーザーの `{id | userPrincipalName}` は、要求を行うために使用された承認トークンにおいてエンコードされたユーザーと一致しなければなりません。

## <a name="function-parameters"></a>関数パラメーター

| パラメーター    | 型   |説明|
|:---------------|:--------|:----------|
|includePersonalNotebooks|Boolean|ユーザーが所有しているノートブックを含みます。 ユーザーが所有しているノートブックを含むには、`true` に設定します。そうでない場合は、`false` に設定します。 `includePersonalNotebooks` パラメーターを含めない場合、要求は `400` エラー応答を返します。|

## <a name="request-headers"></a>要求ヘッダー
| 名前       | 説明|
|:---------------|:----------|
| Authorization  | Bearer {code}|

## <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。

## <a name="response"></a>応答
正常な応答は **recentNotebooks** の JSON コレクションを含む `200 OK` を返します。

## <a name="example"></a>例
次の例は、この API を呼び出す方法を示しています。

##### <a name="request"></a>要求
次の例は要求を示しています。
<!-- { "blockType": "request", "name": "recent_notebooks", "scopes": "notes.read" } -->
```http
GET https://graph.microsoft.com/v1.0/onenote/notebooks/getrecentnotebooks(includePersonalNotebooks=true)
```

##### <a name="response"></a>応答
次の例は応答を示しています。

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1110

{
  "value":[
    {
      "name":"Personal Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDrive"
    },{
      "name":"Team Shared Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDriveForBusiness"
    }
  ]
}
```
