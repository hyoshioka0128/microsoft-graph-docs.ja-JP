---
title: Skype for Business デバイス使用状況レポート
description: Skype for Business デバイス使用状況レポートを使用すると、組織全体で使用されているクライアントやデバイスの種類の詳細を取得できます。 これらの詳細は、組織のための調査、計画、その他のビジネスの意思決定の際に非常に役立ちます。
localization_priority: Normal
ms.prod: reports
author: pranoychaudhuri
ms.openlocfilehash: 8eb1f5896a261610eb5400611a78f5ac75952256
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32565899"
---
# <a name="skype-for-business-device-usage-reports"></a>Skype for Business デバイス使用状況レポート

Skype for Business デバイス使用状況レポートを使用すると、組織全体で使用されているクライアントやデバイスの種類の詳細を取得できます。 これらの詳細は、組織のための調査、計画、その他のビジネスの意思決定の際に非常に役立ちます。

> **注:** 別のレポートのビューとレポート名についての詳細は、「[Office 365 レポート: 使用している Skype for Business クライアント](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3)」を参照してください。

## <a name="reports"></a>レポート

| 関数                                 | 戻り値の型 | 説明                              |
| :--------------------------------------- | :---------- | :--------------------------------------- |
| [ユーザーの詳細を取得する](../api/reportroot-getskypeforbusinessdeviceusageuserdetail.md) | Stream      | ユーザー別の Skype for Business デバイス使用状況に関する詳細を取得します。 |
| [配布のユーザーの数を取得する](../api/reportroot-getskypeforbusinessdeviceusagedistributionusercounts.md) | Stream      | 組織内でそれぞれ別個のデバイスを使用するユーザーの数を取得します。 このレポートでは、Windows、Windows スマートフォン、Android スマートフォン、iPhone、iPad を含むデバイス別のユーザーの数を表示します。 |
| [ユーザーの数を取得する](../api/reportroot-getskypeforbusinessdeviceusageusercounts.md) | Stream      | Skype for Business アプリを使用して接続した組織内のユーザー数について、使用傾向を取得します。 組織内で Skype for Business クライアント アプリをインストールし、使用したデバイスの種類 (Windows、Windows スマートフォン、Android スマートフォン、iPhone、iPad) の詳細も取得できます。 |
