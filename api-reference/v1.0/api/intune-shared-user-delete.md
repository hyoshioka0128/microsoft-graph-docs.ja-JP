---
title: ユーザーを削除する
description: user を削除します。
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e66d987c2e88f40dd5b104961e9203dcd636651a
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32576812"
---
# <a name="delete-user"></a>ユーザーを削除する

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

[user](../resources/intune-shared-user.md) を削除します。

## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。 アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。  必要な特定のアクセス許可は、コンテキストによって異なります。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)| _コンテキストによって異なる_|
| &nbsp;&nbsp;デバイス | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp;&nbsp; MAM | DeviceManagementApps.ReadWrite.All |
| &nbsp;&nbsp;オンボード | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp;トラブルシューティング | DeviceManagementManagedDevices.ReadWrite.All |
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。

## <a name="response"></a>応答
成功した場合、このメソッドは `204 No Content` 応答コードを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。

``` http
DELETE https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。

``` http
HTTP/1.1 204 No Content
```



