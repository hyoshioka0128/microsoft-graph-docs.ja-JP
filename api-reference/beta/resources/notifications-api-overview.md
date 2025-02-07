---
title: Microsoft Graph の REST API 通知を使用する
description: プッシュ通知をユーザーに送信するには、Microsoft Graph の API 通知を使用できます。 ターゲットのユーザー アカウントに通知を送信し、プラットフォームはすべてのデバイスのエンドポイントに通知を配布します。 API 通知の要求は、ユーザーの代理アクセス権と [アクセス権許可の通知]( /graph/permissions_reference)を経由して、Microsoft アカウント、または職場 / 学校のアカウントのどちらでも使用することができます。
localization_priority: Priority
ms.prod: project-rome
ms.openlocfilehash: 28aa795b1df9b2f4817c69332dd8bc9bf3afb172
ms.sourcegitcommit: f80282ff00d5aafc3e575bce447543d7dd23963d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/23/2019
ms.locfileid: "34422522"
---
# <a name="use-the-notifications-rest-api-in-microsoft-graph"></a>Microsoft Graph の REST API 通知を使用する

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

プッシュ通知をユーザーに送信するには、Microsoft Graph の API 通知を使用できます。 ターゲットのユーザー アカウントに通知を送信し、プラットフォームはすべてのデバイスのエンドポイントに通知を配布します。 API 通知の要求は、ユーザーの[代理アクセス権](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions) と[アクセス権許可の通知]( /graph/permissions_reference)を経由して、Microsoft アカウント、または職場 / 学校のアカウントのどちらでも使用することができます。
このユーザー中心の通知は[通知](../resources/projectrome-notification.md)リソースによって表示され、 Microsoft Graph で保存されています。 [クライアント サイド SDK APIs](https://github.com/Microsoft/project-rome)を経由する発行アプリケーションによってアクセスし管理することができます。 

## <a name="next-steps"></a>次の手順
- [通知リソース](../resources/projectrome-notification.md) を参照し、ユーザーに通知を作成します。 
- [Graph エクスプローラー](https://developer.microsoft.com/graph/graph-explorer)で API をお試しください。
- クライアント統合を始めるには、以下に記載されている [統合の概要](/graph/notifications-integration-e2e-overview)の手順を参照してください。
