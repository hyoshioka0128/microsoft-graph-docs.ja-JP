---
title: リスト workingWith
description: ユーザーが作業しているユーザーのリストについて、計算された洞察。
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 906a0f579ff66f7df6d2d5e2b72758cdd397182d
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33334808"
---
# <a name="list-workingwith"></a>リスト workingWith

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

ユーザーが作業しているユーザーのリストについて、計算された洞察。

## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | User.Read.All    |
|委任 (個人用 Microsoft アカウント) | サポートされていません。    |
|アプリケーション | User.Read.All |

## <a name="http-request"></a>HTTP 要求
```http
GET /me/workingWith
GET /users/{id | userPrincipalName}/workingWith
GET /drive/root/createdByUser/workingWith
GET /drive/root/lastModifiedByUser/workingWith
```
## <a name="optional-query-parameters"></a>オプションのクエリ パラメーター
このメソッドは、応答をカスタマイズするための [OData クエリ パラメーター](https://developer.microsoft.com/graph/docs/concepts/query_parameters)をサポートします。

## <a name="request-headers"></a>要求ヘッダー
| ヘッダー         | 値                      |
|:---------------|:---------------------------|
| Authorization  | ベアラー {トークン}。必須。  |
| Content-Type   | application/json           |

## <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。

## <a name="response"></a>応答

成功した場合、このメソッドは 200 OK 応答コードと、応答本文で[User](../resources/user.md)オブジェクトのコレクションを返します。

## <a name="example"></a>例
##### <a name="request"></a>要求
```http
GET https://graph.microsoft.com/beta/me/workingWith
```
##### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 98

{
  "id": "id-value",
  "preferredName": "preferredName-value",
  "Email": "Email-value",
}
```
