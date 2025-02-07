---
title: networkConnection リソースの種類
description: " > **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでは、これらの API の使用はサポートされていません。"
localization_priority: Normal
ms.openlocfilehash: 94bf27265f591d32c01e7043d3a10468a924d78a
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342199"
---
# <a name="networkconnection-resource-type"></a>networkConnection リソースの種類

 [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

通知に関連するネットワーク接続に関するステートフルな情報を含みます。

## <a name="properties"></a>プロパティ

| プロパティ   | 型|説明|
|:---------------|:--------|:----------|
|applicationName|String|ネットワーク接続を管理しているアプリケーションの名前 (例: Facebook、SMTP など)。|
|destinationaddress|String|宛先 IP アドレス (ネットワーク接続の場合)。|
|destinationdomain|String|宛先 URL の宛先ドメイン部分。 (' www.contoso.com ' など)。|
|destinationport|String|宛先ポート (ネットワーク接続の場合)。|
|destinationurl|String|ネットワーク接続 URL/URI 文字列。パラメーターを除外します。 (' www.contoso.com/products/default.html ' など)|
|direction|connectionDirection|ネットワーク接続の方向。 可能な値は、`unknown`、`inbound`、`outbound` です。|
|domainregistereddatetime|DateTimeOffset|宛先ドメインが登録された日付。 Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、必ず UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|
|localDnsName|String|ホストのローカル dns キャッシュに表示されるローカル dns 名解決方法 (たとえば、' hosts ' ファイルが改ざんされた場合)。|
|natDestinationAddress|String|ネットワークアドレス変換先 IP アドレス。|
|natDestinationPort|String|ネットワークアドレス変換先ポート。|
|natSourceAddress|String|ネットワークアドレス変換の送信元 IP アドレス。|
|natSourcePort|String|ネットワークアドレス変換元ポート。|
|プロトコール|securityNetworkProtocol|ネットワークプロトコル。 可能な値: `unknown`、 `ip` `icmp` `igmp` `ggp` `ipv4` `tcp` `pup` `udp` `idp` `ipv6` `ipv6RoutingHeader`、、、、、、、、、、、、 `ipv6FragmentHeader` `ipSecEncapsulatingSecurityPayload` `ipSecAuthenticationHeader` `icmpV6` `ipv6NoNextHeader` `ipv6DestinationOptions` `nd`, `raw`, `ipx`, `spx`, `spxII`.|
|riskScore|String|プロバイダーが生成/計算したネットワーク接続のリスクスコア。 推奨値の範囲0-1。パーセンテージに相当します。|
|sourceaddress|String|ソース (起点) IP アドレス (ネットワーク接続の場合)。|
|sourceport|String|ソース (起点) IP ポート (ネットワーク接続の場合)。|
|status|connectionStatus|ネットワーク接続の状態。 可能な値は、`unknown`、`attempted`、`succeeded`、`blocked`、`failed` です。|
|urlparameters|String|宛先 URL のパラメーター (サフィックス)。|

### <a name="securitynetworkprotocol-values"></a>securitynetworkprotocol の値

|メンバー|値|説明|
|:---|:---|:---|
|不明|-1|不明なプロトコル。|
|ip|.0|インターネットプロトコル。|
|パケット|1-d| インターネットコントロールメッセージプロトコル。|
|igmp|pbm-2| インターネットグループ管理プロトコル。|
|ggp|1/3| ゲートウェイからゲートウェイへのプロトコル。|
|ipv4|2/4| インターネットプロトコルバージョン4。|
|tcp|シックス| 伝送制御プロトコル。|
|.pup|12 | parc ユニバーサルパケットプロトコル。|
|受信|17 | ユーザーデータグラムプロトコル。|
|idp|×| インターネットデータグラムプロトコル。|
|ipv6|41| インターネットプロトコルバージョン 6 (ipv6)。|
|ipv6RoutingHeader|43| ipv6 ルーティングヘッダー。|
|ipv6FragmentHeader|44| ipv6 フラグメントヘッダー。|
|ipSecEncapsulatingSecurityPayload|50| ipv6 カプセル化セキュリティペイロードヘッダー。|
|ipsecauthenticationheader|51| ipv6 認証ヘッダー。|
|過大|58| ipv6 のインターネット制御メッセージプロトコル。|
|ipv6NoNextHeader|59| ipv6 の次のヘッダーはありません。|
|ipv6DestinationOptions|60| ipv6 宛先オプションヘッダー。|
|目|77| ネットディスクプロトコル (非公式)。|
|時|255| 生の IP パケットプロトコル。|
|ipx|1000| インターネットパケット交換プロトコル。|
|spx|1256| 順序付きパケット交換プロトコル。|
|spxii|1257| シーケンス付きパケット交換バージョン2プロトコル。|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.networkConnection"
}-->

```json
{
  "applicationName": "String",
  "destinationAddress": "String",
  "destinationDomain": "String",
  "destinationPort": "String",
  "destinationUrl": "String",
  "direction": "String",
  "domainRegisteredDateTime": "String (timestamp)",
  "localDnsName": "String",
  "natDestinationAddress": "String",
  "natDestinationPort": "String",
  "natSourceAddress": "String",
  "natSourcePort": "String",
  "protocol": "string",
  "riskScore": "String",
  "sourceAddress": "String",
  "sourcePort": "String",
  "status": "String",
  "urlParameters": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "networkConnection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
